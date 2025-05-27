# Discourse Search Banner

A Discourse theme component that adds a customizable search banner with headline and subhead text above the main topic list navigation.

![screenshot](https://user-images.githubusercontent.com/5862206/214549198-419cb28d-efea-43a3-a273-9fd9617de030.png)

## Features

- Customizable search bar with headline and subhead text
- Flexible display options (all pages or homepage only)
- Customizable background image
- Responsive design
- Easy CSS customization

## Installation

1. Visit the [Theme Creator Preview](https://theme-creator.discourse.org/theme/awesomerobot/discourse-search-banner)
2. Follow the [theme component installation guide](https://meta.discourse.org/t/how-do-i-install-a-theme-or-theme-component/63682)

## Configuration

### Display Options

By default, the banner appears on all top-level topic pages including:
- Latest
- New
- Unread
- Top
- Categories
- Any page listed in the `top menu` site setting

You can also configure it to display only on the community's homepage.

### Available Settings

- **Headline and Subhead Text**: Customize the text displayed in the banner
- **Display Location**: Choose between all top-level pages or homepage only
- **Background Image**: Set a custom background image for the banner

### Custom Styling

The component provides two main CSS hooks for customization:

- `.display-search-banner`: Applied to the HTML element where the banner appears
- `.custom-search-banner`: Wraps the banner content

#### Default Custom CSS

```css
/* Sidebar Styling */
.sidebar-container {
  margin-top: 1.5em;
  height: calc(100vh - 3.5em - var(--header-height)) !important;
  overflow-y: auto;
}

.sidebar-container .sidebar-section {
  border-left: 1px solid var(--primary-low);
  margin-top: 0;
  padding-top: 0;
}

#main-outlet {
  min-height: auto;
  overflow: visible;
}

/* New Topic Button Animation */
@keyframes fading-outer-glow {
  0% {
    box-shadow: 0 0 4px 1px rgba(0, 123, 255, 0);
  }
  50% {
    box-shadow: 0 0 6px 2px rgba(0, 123, 255, 0.15);
  }
  100% {
    box-shadow: 0 0 4px 1px rgba(0, 123, 255, 0);
  }
}

button#create-topic {
  position: relative;
  z-index: 1;
  transition: background-color 0.2s ease-in-out, transform 0.1s ease-in-out;
  animation: fading-outer-glow 4s ease-in-out infinite;
}
```

## Roadmap

Future enhancements planned:
- [ ] Category-specific banner display options
- [ ] Additional customization options
- [ ] Enhanced mobile responsiveness

## Credits

This component is based on [angus'](https://github.com/angusmcleod) [header search component](https://meta.discourse.org/t/header-search-theme/67959).

## Links

- [GitHub Repository](https://github.com/discourse/discourse-search-banner)
- [Theme Preview](https://theme-creator.discourse.org/theme/awesomerobot/discourse-search-banner)
- [Installation Guide](https://meta.discourse.org/t/how-do-i-install-a-theme-or-theme-component/63682)

## License

[License information - if applicable]

