<script lang="ts">
    export let href;
    export let iconClass: string = ""; // e.g., 'fab fa-github' for Font Awesome
    export let label;
    export let iconPath = ""; // For SVG path data
</script>

<a
    {href}
    target="_blank"
    rel="noopener noreferrer"
    aria-label={label}
    class="social-icon-link"
>
    {#if iconPath}
        <svg viewBox="0 0 24 24" width="24" height="24" fill="currentColor">
            <path d={iconPath}></path>
        </svg>
    {:else if iconClass}
        <i class={iconClass}></i> <!-- Requires Font Awesome or similar -->
    {/if}
    <span>{label}</span>
</a>

<style>
    .social-icon-link {
        display: inline-flex;
        align-items: center;
        gap: calc(var(--spacing-unit) * 0.75);
        padding: var(--spacing-unit) calc(var(--spacing-unit) * 1.5);
        border: 1px solid var(--border-color);
        border-radius: 20px; /* Pill shape */
        color: var(--text-muted);
        transition: all 0.2s ease-in-out;
        font-size: 0.9em;
    }

    .social-icon-link:hover {
        color: var(--primary-color);
        border-color: var(--primary-color);
        background-color: rgba(
            0,
            224,
            255,
            0.1
        ); /* Slight cyan tint on hover */
        text-decoration: none;
    }

    .social-icon-link svg,
    .social-icon-link i {
        font-size: 1.2em; /* Make icon slightly larger than text */
    }
</style>
