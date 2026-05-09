<script lang="ts">
  import { Github, House, PenLine, FolderCode, Linkedin, BookOpen } from "@lucide/svelte";
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

<Dialog.Root bind:open={dialogOpen}>
  <Dialog.Trigger>
    {#snippet child({ props })}
      <button {...props} class="dialog-trigger">
        <span class="command-button">ctrl</span> +
        <span class="command-button">k</span>
      </button>
    {/snippet}
  </Dialog.Trigger>
  <Dialog.Portal>
    <Dialog.Overlay
      class="data-[state=open]:animate-in data-[state=closed]:animate-out data-[state=closed]:fade-out-0 data-[state=open]:fade-in-0 fixed inset-0 z-50 bg-black/80"
    />
    <Dialog.Content
      class="rounded-card-lg bg-background shadow-popover data-[state=open]:animate-in data-[state=closed]:animate-out data-[state=closed]:fade-out-0 data-[state=open]:fade-in-0 data-[state=closed]:zoom-out-95 data-[state=open]:zoom-in-95  data-[state=closed]:slide-out-to-left-1/2 data-[state=closed]:slide-out-to-top-[48%] data-[state=open]:slide-in-from-left-1/2 data-[state=open]:slide-in-from-top-[48%] outline-hidden fixed left-[50%] top-[50%] z-50 w-full max-w-[94%] translate-x-[-50%] translate-y-[-50%] sm:max-w-[490px] md:w-full"
    >
      <Command.Root
        class="divide-border border-muted bg-background flex h-full w-full flex-col divide-y self-start overflow-hidden rounded-xl border"
      >
        <Command.Input
          class="focus-override h-input bg-background placeholder:text-foreground-alt/50 focus:outline-hidden inline-flex truncate rounded-xl px-4 text-sm transition-colors focus:ring-0"
          placeholder="Rechercher..."
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
                <Command.LinkItem
                  href="./#intro"
                  class="rounded-button data-selected:bg-muted outline-hidden flex h-10 cursor-pointer select-none items-center gap-2 px-3 py-2.5 text-sm capitalize"
                  keywords={["accueil"]}
                >
                  <House class="size-4" />
                  Accueil
                </Command.LinkItem>
                <Command.LinkItem
                  href="./#bts-sio"
                  class="rounded-button data-selected:bg-muted outline-hidden flex h-10 cursor-pointer select-none items-center gap-2 px-3 py-2.5 text-sm capitalize"
                  keywords={["bts", "bts sio", "sio"]}
                >
                  <GraduationCap class="size-4 " />
                  BTS SIO
                </Command.LinkItem>
                <Command.LinkItem
                  href="./#about"
                  class="rounded-button data-selected:bg-muted outline-hidden flex h-10 cursor-pointer select-none items-center gap-2 px-3 py-2.5 text-sm capitalize"
                  keywords={["css", "theme", "colors", "fonts", "tailwind"]}
                >
                  <PenLine class="size-4" />
                  A propos & Experience
                </Command.LinkItem>
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
                <Command.LinkItem
                  href="./#e5"
                  class="rounded-button data-selected:bg-muted outline-hidden flex h-10 cursor-pointer select-none items-center gap-2 px-3 py-2.5 text-sm capitalize"
                  keywords={["bts", "bts sio", "sio", "epreuves", "e5", "E5"]}
                >
                  <FolderCode class="size-4" />
                  Epreuve E5
                </Command.LinkItem>

                <Command.LinkItem
                  href="./#e6"
                  class="rounded-button data-selected:bg-muted outline-hidden flex h-10 cursor-pointer select-none items-center gap-2 px-3 py-2.5 text-sm capitalize"
                  keywords={["bts", "bts sio", "sio", "epreuves", "e6", "E6"]}
                >
                  <FolderCode class="size-4" />
                  Epreuve E6
                </Command.LinkItem>
                <Command.LinkItem
                  href="/Veille"
                  class="rounded-button data-selected:bg-muted outline-hidden flex h-10 cursor-pointer select-none items-center gap-2 px-3 py-2.5 text-sm capitalize"
                  keywords={["veille", "technologique", "computer vision"]}
                >
                  <BookOpen class="size-4" />
                  Veille Technologique
                </Command.LinkItem>
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
                <Command.LinkItem
                  href="https://github.com/ballagye"
                  target="_blank"
                  class="rounded-button data-selected:bg-muted outline-hidden flex h-10 cursor-pointer select-none items-center gap-2 px-3 py-2.5 text-sm capitalize"
                  keywords={["liens", "github", "git", "contact"]}
                >
                  <Github class="size-4" />
                  Github
                </Command.LinkItem>
                <Command.LinkItem
                  value="linkedin"
                  href="https://www.linkedin.com/in/balla-gueye-3b8b6b334/"
                  target="_blank"
                  class="rounded-button data-selected:bg-muted outline-hidden flex h-10 cursor-pointer select-none items-center gap-2 px-3 py-2.5 text-sm capitalize"
                  keywords={["liens", "linked", "linkedin"]}
                >
                  <Linkedin class="size-4" />
                  Linkedin
                </Command.LinkItem>
              </Command.GroupItems>
            </Command.Group>
          </Command.Viewport>
        </Command.List>
      </Command.Root>
    </Dialog.Content>
  </Dialog.Portal>
</Dialog.Root>

<style>
  :global([data-dialog-trigger]) {
    border-radius: 0.5rem;
    background-color: var(--dark-indigo);
    color: var(--light-indigo);

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
    background: var(--indigo);
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
  :global([data-dialog-content][data-state="closed"]) {
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
    display: flex;
    flex-direction: column;
    height: 100%;
    width: 100%;
    align-self: flex-start;
    overflow: hidden;

    background: var(--indigo);
    border: 1px solid var(--light-indigo2);
    border-radius: 0.75rem;
  }

  :global([data-command-root] > * + *) {
    border-top: 1px solid var(--light-indigo2);
  }

  :global([data-command-input]) {
    height: var(--h-input);
    background: var(--indigo);
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;

    font-family: var(--sfpro);
    color: var(--light-indigo2);
    display: inline-flex;
    align-items: center;
    border-radius: 0.75rem;
    padding-left: 1rem;
    padding-right: 1rem;
    font-size: 0.875rem;
    transition:
      color 150ms,
      background-color 150ms,
      border-color 150ms;

    outline: none;
    border: none;
  }
  :global([data-command-input]::placeholder) {
    color: rgba(var(--light-indigo2), 0.5);
  }
  :global([data-command-input]:focus) {
    outline: none;
    box-shadow: none;
  }
  :global([data-command-list]) {
    max-height: 280px;
    overflow-y: auto;
    overflow-x: hidden;
    padding-left: 0.5rem;
    padding-right: 0.5rem;
    padding-bottom: 0.5rem;
  }
  :global([data-command-empty]) {
    color: var(--blue);

    display: flex;
    width: 100%;
    align-items: center;
    justify-content: center;

    padding-top: 2rem;
    padding-bottom: 1.5rem;
    font-size: 0.875rem;
  }
  :global([data-command-group-heading]) {
    font-family: var(--sfpro);
    color: var(--light-indigo2);
    padding-left: 0.75rem;
    padding-right: 0.75rem;
    padding-top: 1rem;
    padding-bottom: 0.5rem;

    font-size: 0.75rem;
  }
  :global([data-command-item]) {
    font-family: var(--sfpro);
    color: var(--light-indigo2);
    border-radius: 0.5rem;
    display: flex;
    align-items: center;
    gap: 0.5rem;
    height: 2.5rem;
    padding-left: 0.75rem;
    padding-right: 0.75rem;
    padding-top: 0.625rem;
    padding-bottom: 0.625rem;
    text-decoration: none;

    font-size: 0.875rem;
    text-transform: capitalize;

    cursor: pointer;
    user-select: none;
    outline: none;
  }
  :global([data-command-item][data-selected=""]) {
    background: var(--dark-indigo);
  }
  .dialog-trigger {
    color: var(--blue);
    background-color: transparent;
    border: 1px solid var(--blue);
    border-radius: var(--border-radius);
    padding: 0.75rem 1rem;
    font-family: var(--ibm);
    line-height: 1;
    text-decoration: none;
    transition: var(--transition);
    margin-left: 15px;
  }

  .dialog-trigger:hover {
    outline: none;
    box-shadow: 3px 3px 0 0 var(--blue);
    transform: translate(-4px, -4px);
  }
  .command-button {
    background-color: var(--dark-indigo);
    padding-left: 6px;
    padding-right: 6px;
    padding-top: 3px;
    padding-bottom: 3px;
    border-radius: 4px;
  }
  .folder-code {
    width: 1px;
    height: 1px;
  }
</style>
