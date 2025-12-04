<script lang="ts">
  import { Github, House, PenLine, FolderCode, Linkedin } from "@lucide/svelte";
  import { Command, Dialog } from "bits-ui";
  import { GraduationCap } from "@lucide/svelte";

  let dialogOpen = $state(false);

  function handleKeydown(e: KeyboardEvent) {
    if (e.key === "k" && (e.metaKey || e.ctrlKey)) {
      e.preventDefault();
      dialogOpen = true;
    }
  }
</script>

<svelte:document onkeydown={handleKeydown} />

<footer>
  <Dialog.Root bind:open={dialogOpen}>
    <Dialog.Trigger
      class="rounded-input bg-dark text-background
        shadow-mini hover:bg-dark/95 focus-visible:ring-foreground focus-visible:ring-offset-background focus-visible:outline-hidden inline-flex
        h-12 select-none items-center justify-center whitespace-nowrap px-[21px] text-[15px] font-semibold transition-colors focus-visible:ring-2 focus-visible:ring-offset-2 active:scale-[0.98]"
    >
      Open Command Menu ctrl + k
    </Dialog.Trigger>
    <Dialog.Portal>
      <Dialog.Overlay
        class="data-[state=open]:animate-in data-[state=closed]:animate-out data-[state=closed]:fade-out-0 data-[state=open]:fade-in-0 fixed inset-0 z-50 bg-black/80"
      />
      <Dialog.Content
        class="rounded-card-lg bg-background shadow-popover data-[state=open]:animate-in data-[state=closed]:animate-out data-[state=closed]:fade-out-0 data-[state=open]:fade-in-0 data-[state=closed]:zoom-out-95 data-[state=open]:zoom-in-95  data-[state=closed]:slide-out-to-left-1/2 data-[state=closed]:slide-out-to-top-[48%] data-[state=open]:slide-in-from-left-1/2 data-[state=open]:slide-in-from-top-[48%] outline-hidden fixed left-[50%] top-[50%] z-50 w-full max-w-[94%] translate-x-[-50%] translate-y-[-50%] sm:max-w-[490px] md:w-full"
      >
        <Dialog.Title class="sr-only">Command Menu</Dialog.Title>
        <Dialog.Description class="sr-only">
          This is the command menu. Use the arrow keys to navigate and press
          ctrl + k to open the search bar.
        </Dialog.Description>
        <Command.Root
          class="divide-border border-muted bg-background flex h-full w-full flex-col divide-y self-start overflow-hidden rounded-xl border"
        >
          <Command.Input
            class="focus-override h-input bg-background placeholder:text-foreground-alt/50 focus:outline-hidden inline-flex truncate rounded-xl px-4 text-sm transition-colors focus:ring-0"
            placeholder="Search for something..."
          />
          <Command.List
            class="max-h-[280px] overflow-y-auto overflow-x-hidden px-2 pb-2"
          >
            <Command.Viewport>
              <Command.Empty
                class="text-muted-foreground flex w-full items-center justify-center pb-6 pt-8 text-sm"
              >
                No results found.
              </Command.Empty>
              <Command.Group>
                <Command.GroupHeading
                  class="text-muted-foreground px-3 pb-2 pt-4 text-xs"
                >
                  Navigation
                </Command.GroupHeading>
                <Command.GroupItems>
                  <Command.Item
                    class="rounded-button data-selected:bg-muted outline-hidden flex h-10 cursor-pointer select-none items-center gap-2 px-3 py-2.5 text-sm capitalize"
                    keywords={["accueil", "bts sio", " a propos", "experience"]}
                  >
                    <House class="size-4" />
                    Accueil
                  </Command.Item>
                  <Command.Item
                    class="rounded-button data-selected:bg-muted outline-hidden flex h-10 cursor-pointer select-none items-center gap-2 px-3 py-2.5 text-sm capitalize"
                    keywords={["child", "custom element", "snippets"]}
                  >
                    <GraduationCap class="size-4 " />
                    BTS SIO
                  </Command.Item>
                  <Command.Item
                    class="rounded-button data-selected:bg-muted outline-hidden flex h-10 cursor-pointer select-none items-center gap-2 px-3 py-2.5 text-sm capitalize"
                    keywords={["css", "theme", "colors", "fonts", "tailwind"]}
                  >
                    <PenLine class="size-4" />
                    A propos & Experience
                  </Command.Item>
                </Command.GroupItems>
              </Command.Group>
              <Command.Separator />
              <Command.Group>
                <Command.GroupHeading
                  class="text-muted-foreground px-3 pb-2 pt-4 text-xs"
                >
                  Epreuves
                </Command.GroupHeading>
                <Command.GroupItems>
                  <Command.Item
                    class="rounded-button data-selected:bg-muted outline-hidden flex h-10 cursor-pointer select-none items-center gap-2 px-3 py-2.5 text-sm capitalize"
                    keywords={["dates", "times"]}
                  >
                    <FolderCode class="size-4" />
                    Epreuve E5
                  </Command.Item>
                  <Command.Item
                    class="rounded-button data-selected:bg-muted outline-hidden flex h-10 cursor-pointer select-none items-center gap-2 px-3 py-2.5 text-sm capitalize"
                    keywords={["buttons", "forms"]}
                  >
                    <FolderCode class="size-4" />
                    Epreuve E6
                  </Command.Item>
                </Command.GroupItems>
              </Command.Group>
              <Command.Separator />
              <Command.Group>
                <Command.GroupHeading
                  class="text-muted-foreground px-3 pb-2 pt-4 text-xs"
                >
                  Liens
                </Command.GroupHeading>
                <Command.GroupItems>
                  <Command.Item
                    class="rounded-button data-selected:bg-muted outline-hidden flex h-10 cursor-pointer select-none items-center gap-2 px-3 py-2.5 text-sm capitalize"
                    keywords={["dates", "times"]}
                  >
                    <Github class="size-4" />
                    Github
                  </Command.Item>
                  <Command.Item
                    class="rounded-button data-selected:bg-muted outline-hidden flex h-10 cursor-pointer select-none items-center gap-2 px-3 py-2.5 text-sm capitalize"
                    keywords={["dates", "times"]}
                  >
                    <Linkedin class="size-4" />
                    LinkedIn
                  </Command.Item>
                </Command.GroupItems>
              </Command.Group>
            </Command.Viewport>
          </Command.List>
        </Command.Root>
      </Dialog.Content>
    </Dialog.Portal>
  </Dialog.Root>
</footer>

<style>
  :global([data-dialog-trigger]) {
    border-radius: 0.5rem;
    background-color: #0f0f0f;
    color: var(--blue);
    box-shadow: 0 1px 2px rgba(0, 0, 0, 0.15);

    display: inline-flex;
    height: 3rem;
    user-select: none;
    align-items: center;
    justify-content: center;
    white-space: nowrap;

    padding-left: 21px;
    padding-right: 21px;

    font-size: 15px;
    font-weight: 600;

    transition:
      color 150ms,
      background-color 150ms,
      border-color 150ms,
      box-shadow 150ms;
  }

  :global([data-dialog-overlay][data-state="open"]) {
    animation: fadeIn 0.2s ease-out forwards;
  }

  :global([data-dialog-overlay][data-state="closed"]) {
    animation: fadeOut 0.2s ease-in forwards;
  }

  :global([data-dialog-overlay]) {
    position: fixed;
    inset: 0;
    z-index: 50;
    background-color: rgba(0, 0, 0, 0.8);
  }

  @keyframes fadeIn {
    from {
      opacity: 0;
    }
    to {
      opacity: 1;
    }
  }

  @keyframes fadeOut {
    from {
      opacity: 1;
    }
    to {
      opacity: 0;
    }
  }

  :global([data-dialog-content]) {
    border-radius: 1rem;
    background: var(--background);
    box-shadow: 0px 4px 24px rgba(0, 0, 0, 0.12);
    outline: none;

    position: fixed;

    left: 50%;
    top: 50%;

    z-index: 50;

    width: 100%;
    max-width: 94%;
    transform: translate(-50%, -50%);
  }

  @media (min-width: 640px) {
    :global([data-dialog-content]) {
      max-width: 490px;
    }
  }

  @media (min-width: 768px) {
    :global([data-dialog-content]) {
      width: 100%;
    }
  }

  :global([data-dialog-content][data-state="open"]) {
    animation:
      fadeIn 0.25s ease-out forwards,
      zoomIn 0.25s ease-out forwards,
      slideInLeft 0.25s ease-out forwards,
      slideInTop 0.25s ease-out forwards;
  }
  :global([data-dialog-content][data-state="open"]) {
    animation:
      fadeOut 0.2s ease-in forwards,
      zoomOut 0.2s ease-in forwards,
      slideOutLeft 0.2s ease-in forwards,
      slideOutTop 0.2s ease-in forwards;
  }
  @keyframes fadeIn {
    from {
      opacity: 0;
    }
    to {
      opacity: 1;
    }
  }

  @keyframes fadeOut {
    from {
      opacity: 1;
    }
    to {
      opacity: 0;
    }
  }
  @keyframes zoomIn {
    from {
      transform: translate(-50%, -50%) scale(0.95);
    }
    to {
      transform: translate(-50%, -50%) scale(1);
    }
  }

  @keyframes zoomOut {
    from {
      transform: translate(-50%, -50%) scale(1);
    }
    to {
      transform: translate(-50%, -50%) scale(0.95);
    }
  }
  @keyframes slideInLeft {
    from {
      transform: translate(calc(-50% - 50%), -50%);
    }
    to {
      transform: translate(-50%, -50%);
    }
  }

  @keyframes slideOutLeft {
    from {
      transform: translate(-50%, -50%);
    }
    to {
      transform: translate(calc(-50% - 50%), -50%);
    }
  }
  @keyframes slideInTop {
    from {
      transform: translate(-50%, calc(-50% - 48%));
    }
    to {
      transform: translate(-50%, -50%);
    }
  }

  @keyframes slideOutTop {
    from {
      transform: translate(-50%, -50%);
    }
    to {
      transform: translate(-50%, calc(-50% - 48%));
    }
  }
  :global([data-command-root]) {
    display: flex; /* flex */
    flex-direction: column; /* flex-col */
    height: 100%; /* h-full */
    width: 100%; /* w-full */
    align-self: flex-start; /* self-start */
    overflow: hidden; /* overflow-hidden */

    /* Style */
    background: var(--indigo); /* bg-background */
    border: 1px solid var(--border-muted); /* border + border-muted */
    border-radius: 0.75rem; /* rounded-xl */
    border-top: 1px solid var(--border);
  }
  :global([data-command-input]) {
    height: var(
      --h-input,
      2.5rem
    ); /* h-input — mets la valeur exacte si tu veux */
    background: var(--background); /* bg-background */
    overflow: hidden; /* truncate */
    text-overflow: ellipsis;
    white-space: nowrap;

    display: inline-flex; /* inline-flex */
    align-items: center;
    border-radius: 0.75rem; /* rounded-xl */
    padding-left: 1rem; /* px-4 */
    padding-right: 1rem;
    font-size: 0.875rem; /* text-sm */
    color: inherit;
    transition:
      color 150ms,
      background-color 150ms,
      border-color 150ms;

    outline: none; /* focus:outline-hidden */
    border: none;
  }
  :global([data-command-input]::placeholder) {
    color: rgba(var(--foreground-alt-rgb), 0.5);
  }
  :global([data-command-input]:focus) {
    outline: none;
    box-shadow: none;
  }
  :global([data-command-list]) {
    max-height: 280px; /* max-h-[280px] */
    overflow-y: auto; /* overflow-y-auto */
    overflow-x: hidden; /* overflow-x-hidden */
    padding-left: 0.5rem; /* px-2 */
    padding-right: 0.5rem; /* px-2 */
    padding-bottom: 0.5rem; /* pb-2 */
  }
  :global([data-command-empty]) {
    color: var(--blue); /* text-muted-foreground */

    display: flex; /* flex */
    width: 100%; /* w-full */
    align-items: center; /* items-center */
    justify-content: center; /* justify-center */

    padding-top: 2rem; /* pt-8  (8 × 0.25rem) */
    padding-bottom: 1.5rem; /* pb-6  (6 × 0.25rem) */

    font-size: 0.875rem; /* text-sm */
  }
  :global([data-command-group-heading]) {
    color: var(--muted-foreground); /* text-muted-foreground */

    padding-left: 0.75rem; /* px-3 */
    padding-right: 0.75rem; /* px-3 */
    padding-top: 1rem; /* pt-4 */
    padding-bottom: 0.5rem; /* pb-2 */

    font-size: 0.75rem; /* text-xs */
  }
  :global([data-command-item]) {
    border-radius: 0.5rem; /* rounded-button */
    display: flex; /* flex */
    align-items: center; /* items-center */
    gap: 0.5rem; /* gap-2 */

    height: 2.5rem; /* h-10 */
    padding-left: 0.75rem; /* px-3 */
    padding-right: 0.75rem; /* px-3 */
    padding-top: 0.625rem; /* py-2.5 */
    padding-bottom: 0.625rem; /* py-2.5 */

    font-size: 0.875rem; /* text-sm */
    text-transform: capitalize; /* capitalize */

    cursor: pointer; /* cursor-pointer */
    user-select: none; /* select-none */
    outline: none;
  }
  :global([data-command-item][data-selected="true"]) {
    background: var(--dark-indigo);
  }
</style>
