<script>
    export let onNavigate;
</script>

<div class="home-container container text-center">
    <img src="/images/me.avif" alt="Theo Paris" class="profile-image-large" />

    <h1>Hello there.</h1>

    <p class="welcome-text">
        I'm Theo, and I'm a 20-year-old programmer and music producer.
    </p>

    <button class="btn" on:click={() => onNavigate("about")}>
        Learn More About Me
    </button>
</div>

<style>
    .home-container {
        padding-top: calc(var(--spacing-unit) * 5);
        padding-bottom: calc(var(--spacing-unit) * 5);
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .profile-image-large {
        width: 200px;
        height: 200px;
        border-radius: 50%; /* Circular image */
        object-fit: cover;
        margin-bottom: calc(var(--spacing-unit) * 3);
        border: 4px solid var(--primary-color);
        box-shadow: 0 0 15px rgba(0, 224, 255, 0.3);
    }

    h1 {
        font-size: 3em; /* Larger than other h1 for impact */
        margin-bottom: calc(var(--spacing-unit) * 1);
    }

    .welcome-text {
        font-size: 1.2em;
        color: var(--text-muted);
        max-width: 600px;
        margin-bottom: calc(var(--spacing-unit) * 4);
    }

    .btn {
        margin-bottom: calc(var(--spacing-unit) * 5);
    }

    .quick-info {
        margin-top: calc(var(--spacing-unit) * 3);
        display: flex;
        align-items: center;
        gap: var(--spacing-unit) * 2;
        padding: var(--spacing-unit) * 2;
        background-color: var(--card-background);
        border-radius: 8px;
        max-width: 500px;
    }

    .mc-avatar {
        width: 60px;
        height: 60px;
        border-radius: 8px;
    }

    .quick-info p {
        margin: 0;
        font-size: 0.9em;
        text-align: left;
        color: var(--text-muted);
    }

    @media (max-width: 600px) {
        h1 {
            font-size: 2.5em;
        }
        .profile-image-large {
            width: 150px;
            height: 150px;
        }
        .quick-info {
            flex-direction: column;
            text-align: center;
        }
        .quick-info p {
            text-align: center;
        }
    }
</style>
