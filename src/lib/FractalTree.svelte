<script lang="ts">
  import { onMount } from "svelte";
  import p5 from "p5";

  let container: HTMLDivElement;

  onMount(() => {
    const sketch = (p: p5) => {
      const SIZE = 400;
      const MAX_DEPTH = 13;

      function tree(
        x: number,
        y: number,
        length: number,
        direction: number,
        depth: number,
        bendAmount: number
      ) {
        if (depth > MAX_DEPTH) return;

        p.strokeWeight(length / 15);
        p.stroke(255);

        let dir = direction;
        if (depth > 0) dir += bendAmount;

        const rad = p.radians(dir);
        const x2 = x + Math.cos(rad) * length;
        const y2 = y + Math.sin(rad) * length;

        p.line(x, y, x2, y2);

        tree(x2, y2, length * 0.9, direction + 25, depth + 1, bendAmount);
        tree(x2, y2, length * 0.45, direction - 90, depth + 1, bendAmount);
      }

      p.setup = () => {
        p.createCanvas(SIZE, SIZE);
        p.frameRate(60);
        p.pixelDensity(3);
      };

      p.draw = () => {
        p.background("#1E1A4D");

        p.push();
        p.translate(SIZE / 2, SIZE / 2);
        p.scale(1, -1);
        p.scale(0.14);

        const t = p.frameCount * 0.01;
        const bendAmount = Math.sin(t) * 20;

        tree(400, -500, 300, 90, 0, bendAmount);

        p.pop();
      };
    };

    const instance = new p5(sketch, container);
    return () => instance.remove();
  });
</script>

<div class="fractal-container" bind:this={container}></div>
