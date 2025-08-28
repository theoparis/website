<script>
    import SocialLink from "../components/SocialLink.svelte";

    // SVG path data for icons (example for GitHub, replace with actuals or use Font Awesome)
    // Find these on sites like materialdesignicons.com or feathericons.com
    const githubIconPath =
        "M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12";
    const twitterIconPath =
        "M23.953 4.57a10 10 0 01-2.825.775 4.958 4.958 0 002.163-2.723c-.951.555-2.005.959-3.127 1.184a4.92 4.92 0 00-8.384 4.482C7.69 8.095 4.067 6.13 1.64 3.162a4.822 4.822 0 00-.666 2.475c0 1.71.87 3.213 2.188 4.096a4.904 4.904 0 01-2.228-.616v.06a4.923 4.923 0 003.946 4.827 4.996 4.996 0 01-2.212.085 4.936 4.936 0 004.604 3.417 9.867 9.867 0 01-6.102 2.105c-.39 0-.779-.023-1.17-.067a13.995 13.995 0 007.557 2.209c9.053 0 13.998-7.496 13.998-13.985 0-.21 0-.42-.015-.63A9.935 9.935 0 0024 4.59z";
    const youtubeIconPath =
        "M23.498 6.186a3.016 3.016 0 00-2.122-2.136C19.505 3.545 12 3.545 12 3.545s-7.505 0-9.377.505A3.017 3.017 0 00.502 6.186C0 8.07 0 12 0 12s0 3.93.502 5.814a3.016 3.016 0 002.122 2.136c1.871.505 9.376.505 9.376.505s7.505 0 9.377-.505a3.015 3.015 0 002.122-2.136C24 15.93 24 12 24 12s0-3.93-.502-5.814zM9.545 15.568V8.432L15.818 12l-6.273 3.568z";
    const emailIconPath =
        "M22 6c0-1.1-.9-2-2-2H4c-1.1 0-2 .9-2 2v12c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6zm-2 0l-8 5-8-5h16zm0 12H4V8l8 5 8-5v10z";
</script>

<div class="about-container container">
    <div class="about-header">
        <div class="about-images">
            <img
                src="/images/me.avif"
                alt="Theo Paris"
                class="about-profile-image"
            />
            <img
                src="/images/ruby.avif"
                alt="Ruby, Theo's dog"
                class="about-profile-image"
            />
        </div>
        <h2>About Me</h2>
    </div>

    <section class="content-section">
        <p>
            My name is Theo. I am 21 years old and I love programming and
            producing music! My favorite video game is Minecraft.
        </p>
    </section>

    <section class="content-section">
        <h3>Programming</h3>
        <p>
            I have been coding since I was 12, and have worked with many
            programming languages. My favorite programming languages are
            TypeScript, C++ and Rust. I have also worked with frameworks such as
            Svelte and databases like Postgres. I am mostly self-taught, however
            I have taken a college-level C++ class.
        </p>
    </section>

    <section class="content-section">
        <h3>Social Media & Contact</h3>
        <div class="social-links-grid">
            <SocialLink
                href="https://github.com/theoparis"
                label="GitHub"
                iconPath={githubIconPath}
            />
            <SocialLink
                href="https://x.com/TheoParis04"
                label="Twitter"
                iconPath={twitterIconPath}
            />
            <SocialLink
                href="https://youtube.com/@TheoParis"
                label="YouTube"
                iconPath={youtubeIconPath}
            />
            <SocialLink
                href="mailto:theo@theoparis.com"
                label="Email"
                iconPath={emailIconPath}
            />
        </div>
        <p class="contact-note">
            If you are looking for a way to contact me, you can email me using <a
                href="theo@theoparis.com">theo@theoparis.com</a
            >. You can also contact me through discord with my username:
            <strong>theoparis</strong>.
        </p>
    </section>
</div>

<style>
    .about-container {
        padding-top: calc(var(--spacing-unit) * 3);
        padding-bottom: calc(var(--spacing-unit) * 5);
    }

    .about-header {
        text-align: center;
        margin-bottom: calc(var(--spacing-unit) * 4);
    }

    .about-images {
        display: flex;
        justify-content: center;
        gap: calc(var(--spacing-unit) * 3);
        margin-bottom: calc(var(--spacing-unit) * 2);
    }

    .about-profile-image {
        width: 150px;
        height: 150px;
        object-fit: cover;
        border-radius: 50%; /* Circular images */
        border: 3px solid var(--primary-color);
    }

    .about-header h2 {
        margin-top: var(
            --spacing-unit
        ); /* reduce top margin if images are above */
    }

    .content-section {
        background-color: var(--card-background);
        padding: calc(var(--spacing-unit) * 2.5);
        border-radius: 8px;
        margin-bottom: calc(var(--spacing-unit) * 3);
        box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
    }

    .content-section h3 {
        margin-top: 0; /* First element in section */
        border-bottom: 1px solid var(--border-color);
        padding-bottom: var(--spacing-unit);
        margin-bottom: calc(var(--spacing-unit) * 2);
    }

    .content-section p {
        color: var(--text-muted);
        line-height: 1.7;
    }
    .content-section p:last-child {
        margin-bottom: 0;
    }

    .social-links-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
        gap: calc(var(--spacing-unit) * 1.5);
        margin-bottom: calc(var(--spacing-unit) * 2.5);
    }

    .contact-note {
        font-size: 0.9em;
        margin-top: calc(var(--spacing-unit) * 2);
    }
    .contact-note strong {
        color: var(--text-color);
    }

    @media (max-width: 768px) {
        .about-profile-image {
            width: 120px;
            height: 120px;
        }
    }
    @media (max-width: 480px) {
        .about-images {
            flex-direction: column;
            align-items: center;
        }
        .about-profile-image {
            width: 130px;
            height: 130px;
        }
        .social-links-grid {
            grid-template-columns: 1fr; /* Stack social links on very small screens */
        }
    }
</style>
