# Accessible Modal System

A lightweight, accessible modal dialog system that follows WCAG accessibility guidelines. This solution provides a responsive modal window system with keyboard navigation, focus management, and screen reader support.

## Features

- ✨ Fully accessible with ARIA attributes and keyboard support
- 🎯 Focus trap management
- 📱 Responsive design with multiple size options
- 🎥 Support for video content (YouTube)
- ⌨️ Complete keyboard navigation
- 🔒 Body scroll lock when modal is open
- 🎨 Customizable styling
- 🔍 Screen reader friendly

## Installation

1. Include the CSS file in your HTML:
```html
<link rel="stylesheet" href="path/to/accessible-modals.css">
```

2. Include the JavaScript file before the closing `</body>` tag:
```html
<script src="path/to/accessible-modals.js"></script>
```

3. Add the modal cover div to your HTML:
```html
<div class="modal-cover"></div>
```

## Usage

### Basic Modal Structure

```html
<div id="yourModalId" class="modal-dialog modal-large" role="dialog" aria-modal="true" aria-labelledby="titleId">
    <div class="modal-dialog-wrap">
        <div class="modal-dialog-content">
            <h2 id="titleId" tabindex="-1" class="dialog-label">Modal Title</h2>
            <!-- Your modal content here -->
        </div>
        <button class="modal-close" aria-label="Close modal">&times;</button>
    </div>
</div>
```

### Trigger Button

```html
<a href="#" role="button" class="modal-trigger" data-reveal-id="yourModalId">Open Modal</a>
```

## Size Options

The system supports three modal sizes:
- Large: `modal-large` (778px max-width)
- Medium: `modal-medium` (568px max-width)
- Small: `modal-small` (368px max-width)

## Video Support

For YouTube videos, use the following structure:

```html
<div id="videoModalId" class="modal-dialog modal-large" role="dialog" aria-modal="true" aria-labelledby="videoTitle">
    <div class="modal-dialog-wrap">
        <div class="modal-dialog-content">
            <h2 class="sr-only" tabindex="-1">Video Title</h2>
            <iframe src="" data-src="https://www.youtube.com/embed/VIDEO_ID?rel=0&amp;autoplay=1" 
                    width="100%" height="531" frameborder="0" 
                    allowfullscreen="allowfullscreen"></iframe>
        </div>
        <button class="modal-close" aria-label="Close modal">&times;</button>
    </div>
</div>
```

## Accessibility Features

### Keyboard Support
- `Escape` key closes the modal
- `Tab` cycles through focusable elements within the modal
- `Shift + Tab` cycles backwards through focusable elements
- Focus is trapped within the modal while open
- Focus returns to trigger element when closed

### ARIA Attributes
- `role="dialog"` identifies the modal
- `aria-modal="true"` indicates modal behavior
- `aria-labelledby` associates the modal with its title
- `aria-label` provides accessible names for buttons

### Focus Management
- Automatic focus on first focusable element or modal title
- Focus trap within modal while open
- Focus restoration when modal closes
- Custom focus handling for video content

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- IE11 (basic support)

## CSS Customization

The modal system uses CSS variables for easy customization. Key classes:

- `.modal-dialog` - Main modal container
- `.modal-dialog-content` - Content wrapper
- `.modal-close` - Close button
- `.modal-cover` - Background overlay

## Events

The system triggers the following events:
- Modal open
- Modal close
- Video load (for YouTube embeds)

## License

MIT License - feel free to use in personal and commercial projects.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.