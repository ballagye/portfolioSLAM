<script lang="ts">
  import { onMount } from "svelte";

  type Article = {
    number: string;
    title: string;
    subtitle: string;
    description: string;
    date: string;
    tags: string[];
    link: string;
    video: string;
  };

  const articles: Article[] = [
    {
      number: "01",
      title: "Detect IA Tag",
      subtitle: "RATP / Computer Vision",
      description:
        "En octobre 2025, la RATP a dévoilé son projet Detect IA Tag. Des caméras intelligentes analysent les rames en mouvement dans les tunnels du métro parisien. En 7 secondes, le système scanne un train complet et génère un rapport précis : surface graffitée, état par voiture, horodatage.",
      date: "Octobre 2025",
      tags: ["Transports", "Edge Computing", "Détection temps réel"],
      link: "https://www.lemagit.fr/actualites/366633953/Detect-IA-Tag-la-RATP-chasse-les-graffitis-avec-sa-Computer-Vision",
      video: "/ratparticle.mp4",
    },
    {
      number: "02",
      title: "Computer Vision en médecine",
      subtitle: "Santé / Deep Learning",
      description:
        "Publié en août 2025, l'article de Brady Magazine explore les applications concrètes de la Computer Vision dans la santé et l'industrie. En médecine, ces systèmes analysent radiographies, IRM et scanners pour détecter des maladies avec une précision comparable à celle d'un spécialiste. Dans l'industrie, ils automatisent le contrôle qualité en identifiant des défauts à une vitesse inégalée par l'œil humain.",
      date: "Août 2025",
      tags: ["Santé", "Imagerie médicale", "Diagnostic"],
      link: "https://www.brady-magazine.com/vision-par-ordinateur-quelles-applications-dans-la-sante-et-lindustrie",
      video: "/medecinearticle.mp4",
    },
  ];

  let currentIndex = $state(0);
  let wrapper: HTMLElement;
  let animating = $state(false);

  function goTo(index: number) {
    if (animating || index === currentIndex) return;
    animating = true;
    currentIndex = index;
    setTimeout(() => (animating = false), 400);
  }

  onMount(() => {
    const total = articles.length;

    const observer = new IntersectionObserver(
      (entries) => {
        entries.forEach((entry) => {
          if (entry.isIntersecting) {
            wrapper.addEventListener("wheel", handleWheel, { passive: false });
          } else {
            wrapper.removeEventListener("wheel", handleWheel);
          }
        });
      },
      { threshold: 0.5 },
    );

    observer.observe(wrapper);

    function handleWheel(e: WheelEvent) {
      if (e.deltaY > 0 && currentIndex < total - 1) {
        e.preventDefault();
        goTo(currentIndex + 1);
      } else if (e.deltaY < 0 && currentIndex > 0) {
        e.preventDefault();
        goTo(currentIndex - 1);
      }
    }

    return () => {
      observer.disconnect();
      wrapper.removeEventListener("wheel", handleWheel);
    };
  });
</script>

<div class="articles-wrapper" bind:this={wrapper}>
  <div class="articles-inner">
    <div class="image-side">
      {#each articles as article, i}
        <div class="image-frame" class:active={currentIndex === i}>
          <video src={article.video} muted autoplay loop playsinline> </video>
          <a href={article.link} target="_blank" class="view-btn">Consulter</a>
        </div>
      {/each}
    </div>

    <div class="content-side">
      {#each articles as article, i}
        <div class="article-content" class:active={currentIndex === i}>
          <p class="counter">
            [ {article.number} / {String(articles.length).padStart(2, "0")} ]
          </p>
          <h2 class="article-title">{article.title}</h2>
          <p class="article-subtitle">{article.subtitle}</p>
          <p class="article-desc">{article.description}</p>
          <p class="article-date">{article.date}</p>
          <div class="tags">
            {#each article.tags as tag}
              <span class="cards">{tag}</span>
            {/each}
          </div>
          <a href={article.link} target="_blank" class="article-link">
            Lire l'article →
          </a>
        </div>
      {/each}
    </div>
  </div>
</div>

<style>
  .articles-wrapper {
    position: sticky;
    top: 0;
    height: 100%;
    overflow: hidden;
    max-width: 100%;
    margin: 0 auto;
    padding-bottom: 100px;
  }

  .articles-inner {
    display: flex;
    align-items: center;
    height: 100%;
    gap: 80px;
    padding: 0 40px;
  }

  .image-side {
    position: relative;
    width: 55%;
    flex-shrink: 0;
    height: 420px;
  }

  .image-frame {
    position: absolute;
    inset: 0;
    border-radius: 12px;
    overflow: hidden;
    opacity: 0;
    transform: translateY(20px);
    transition:
      opacity 400ms ease,
      transform 400ms ease;
    pointer-events: none;
  }

  .image-frame.active {
    opacity: 1;
    transform: translateY(0);
    pointer-events: all;
  }

  .image-frame video {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  .view-btn {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%) scale(0.8);
    background: white;
    color: black;
    font-family: var(--sfpro);
    font-size: 14px;
    font-weight: 600;
    padding: 14px 28px;
    border-radius: 50px;
    text-decoration: none;
    opacity: 0;
    transition:
      opacity 200ms ease,
      transform 200ms ease;
    letter-spacing: 0.1em;
  }

  .image-frame:hover .view-btn {
    opacity: 1;
    transform: translate(-50%, -50%) scale(1);
  }

  .content-side {
    position: relative;
    flex: 1;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  .article-content {
    position: absolute;
    inset: 0;
    display: flex;
    flex-direction: column;
    justify-content: center;
    opacity: 0;
    transform: translateY(16px);
    transition:
      opacity 400ms ease,
      transform 400ms ease;
    pointer-events: none;
  }

  .article-content.active {
    opacity: 1;
    transform: translateY(0);
    pointer-events: all;
  }

  .counter {
    font-family: var(--sfpro);
    font-size: 14px;
    opacity: 0.5;
    margin: 0 0 16px;
    letter-spacing: 0.05em;
  }

  .article-title {
    font-family: var(--sfpro);
    font-size: 2.2rem;
    font-weight: 700;
    margin: 0 0 6px;
    color: var(--blue);
  }

  .article-subtitle {
    font-family: var(--sfpro);
    font-size: 1rem;
    opacity: 0.6;
    margin: 0 0 20px;
  }

  .article-desc {
    font-family: var(--sfpro);
    font-size: 1rem;
    line-height: 1.7;
    margin: 0 0 16px;
  }

  .article-date {
    font-family: var(--sfpro);
    font-size: 0.85rem;
    opacity: 0.45;
    margin: 0 0 16px;
  }

  .tags {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
    margin-bottom: 24px;
  }

  .cards {
    display: inline-block;
    padding: 0.25rem 0.75rem;
    background: var(--indigo-dark);
    color: var(--white);
    border: 1px solid var(--blue);
    border-radius: 4px;
    font-size: 0.8rem;
    font-family: var(--sfpro);
  }

  .article-link {
    font-family: var(--sfpro);
    font-size: 0.9rem;
    color: var(--blue);
    text-decoration: none;
    letter-spacing: 0.02em;
    transition: opacity 150ms ease;
    align-self: flex-start;
  }

  .article-link:hover {
    opacity: 0.7;
  }
</style>
