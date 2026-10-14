---
{
  "scope": "The pinkary.com web application at d6b01b7a717ac28177c26776266011eaab35f696: public and signed-in web pages, their Livewire components, actions, policies, queries, notifications and scheduled commands.",
  "method": "Read-only static inspection of routes, controllers, Livewire components, actions, policies, queries, models, observers, scheduled commands and Blade views.",
  "covered": [
    {
      "description": "Web, authentication and schedule routes.",
      "paths": [
        "routes/web.php",
        "routes/auth.php",
        "routes/console.php"
      ]
    },
    {
      "description": "Web controllers, middleware, form requests and the home feed response.",
      "paths": [
        "app/Http/Controllers/Auth/",
        "app/Http/Controllers/AccountController.php",
        "app/Http/Controllers/AccountLogoutAllController.php",
        "app/Http/Controllers/AccountRemoveController.php",
        "app/Http/Controllers/BookmarksController.php",
        "app/Http/Controllers/ChannelController.php",
        "app/Http/Controllers/HashtagController.php",
        "app/Http/Controllers/HomeController.php",
        "app/Http/Controllers/NotificationController.php",
        "app/Http/Controllers/QrCodeController.php",
        "app/Http/Controllers/QuestionController.php",
        "app/Http/Controllers/UserAvatarController.php",
        "app/Http/Controllers/UserController.php",
        "app/Http/Controllers/UserGitHubUsernameController.php",
        "app/Http/Controllers/UserIsVerifiedController.php",
        "app/Http/Middleware/",
        "app/Http/Requests/UserUpdateRequest.php",
        "app/Http/Requests/UserAvatarUpdateRequest.php",
        "app/Http/Responses/"
      ]
    },
    {
      "description": "Livewire components and their views.",
      "paths": [
        "app/Livewire/",
        "resources/views/livewire/"
      ]
    },
    {
      "description": "Domain actions, policies, observers, rules, models and enums.",
      "paths": [
        "app/Actions/",
        "app/Policies/",
        "app/Observers/",
        "app/Rules/",
        "app/Models/",
        "app/Enums/"
      ]
    },
    {
      "description": "Feed and profile queries.",
      "paths": [
        "app/Queries/"
      ]
    },
    {
      "description": "Notifications, the notification email and scheduled commands and jobs.",
      "paths": [
        "app/Notifications/",
        "app/Mail/",
        "app/Console/Commands/",
        "app/Jobs/"
      ]
    },
    {
      "description": "Account switching, verified-badge, avatar, QR code and view-counting services.",
      "paths": [
        "app/Services/Accounts.php",
        "app/Services/GitHub.php",
        "app/Services/Avatar.php",
        "app/Services/QrCode.php",
        "app/Services/Firewall.php",
        "app/Providers/FortifyServiceProvider.php"
      ]
    },
    {
      "description": "Page and form templates.",
      "paths": [
        "resources/views/auth/",
        "resources/views/profile/",
        "resources/views/home/",
        "resources/views/questions/",
        "resources/views/channels/",
        "resources/views/hashtag/",
        "resources/views/notifications/",
        "resources/views/bookmarks/",
        "resources/views/layouts/",
        "resources/views/components/"
      ]
    }
  ],
  "exclusions": [
    {
      "description": "Tests, factories, seeders and migrations.",
      "paths": [
        "tests/",
        "database/"
      ]
    },
    {
      "description": "Build, styling, front-end assets, fonts and static images.",
      "paths": [
        "resources/css/",
        "resources/js/",
        "public/",
        "vite.config.js",
        "package.json"
      ]
    },
    {
      "description": "Tooling, configuration, contributor and agent rules.",
      "paths": [
        ".ai/",
        ".hod/",
        ".github/",
        "config/",
        "bootstrap/",
        "composer.json",
        "phpstan.neon",
        "rector.php",
        "pint.json",
        "phpunit.xml",
        "docker-compose.yml"
      ]
    },
    {
      "description": "Content parsing and rendering of links, mentions, hashtags, code and images, autocomplete and link previews.",
      "paths": [
        "app/Services/ParsableContent.php",
        "app/Services/ParsableContentProviders/",
        "app/Services/ParsableBio.php",
        "app/Services/Autocomplete.php",
        "app/Services/Autocomplete/",
        "app/Services/MetaData.php",
        "app/Services/SafeUrlFetcher.php",
        "app/Services/BoundedResponseBody.php",
        "app/Services/FeedContent.php",
        "app/Services/ImageProcessor.php"
      ]
    }
  ],
  "unmapped": [
    {
      "description": "The in-development mobile API and its controllers, requests, resources and captcha.",
      "paths": [
        "routes/api.php",
        "routes/api/",
        "app/Http/Controllers/Api/",
        "app/Http/Requests/Api/",
        "app/Http/Resources/",
        "app/Services/MobileCaptcha.php",
        "app/Services/TwoFactorChallenge.php",
        "app/Rules/MobileTurnstile.php"
      ]
    },
    {
      "description": "The administration panel for moderation, users, blocked accounts and suppressed emails.",
      "paths": [
        "app/Filament/",
        "app/Providers/Filament/",
        "resources/views/filament/"
      ]
    },
    {
      "description": "Static pages, changelog, people-to-follow suggestions and image clean-up jobs.",
      "paths": [
        "resources/views/about.blade.php",
        "resources/views/changelog.blade.php",
        "resources/views/terms.blade.php",
        "resources/views/privacy.blade.php",
        "resources/views/support.blade.php",
        "resources/views/brand/",
        "resources/views/verified.blade.php",
        "app/Http/Controllers/ChangelogController.php",
        "app/Services/Changelog.php",
        "app/Services/Git.php",
        "app/Services/PeopleToFollowRecommendations.php"
      ]
    }
  ],
  "limitations": [
    {
      "description": "Sponsorship lookups and Turnstile challenges depend on external services whose answers source cannot establish.",
      "paths": [
        "app/Services/GitHub.php",
        "app/Http/Controllers/Auth/RegisteredUserController.php"
      ]
    }
  ]
}
---

# Coverage
