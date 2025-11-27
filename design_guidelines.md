# SmartStay Design Guidelines

## Design Approach
**Design System Approach** - Using a custom design system derived from Material Design principles, optimized for smart home control applications with clear visual feedback and information density.

## Core Design Principles
1. **Clarity First**: Device states and controls must be immediately recognizable
2. **Consistent Feedback**: Every interaction provides visual confirmation
3. **Seamless Transition**: Landing page to dashboard feels like one unified product
4. **Trust & Reliability**: Professional aesthetic that conveys stability and security

## Typography System
**Font Family**: Inter (Google Fonts)
- Headings: 700 weight
- Subheadings: 600 weight  
- Body: 400 weight
- UI Elements: 500-600 weight

**Scale**:
- H1: 48px (Hero headlines)
- H2: 32px (Section titles)
- H3: 24px (Card titles, room names)
- Body: 16px
- Small: 14px (metadata, labels)
- Micro: 13px (chips, badges)

## Layout & Spacing System
**Container**: max-width 1440px, centered with 120px horizontal padding (desktop), 16px (mobile)

**Spacing Units** (Tailwind):
- Micro spacing: 2, 4 (gaps, padding within components)
- Standard spacing: 6, 8, 12 (component padding, card spacing)
- Section spacing: 16, 20 (section vertical padding)
- Large spacing: 24, 32 (major section separation)

**Grid System**:
- Landing page features: 3 columns (desktop), 1 column (mobile)
- Dashboard devices: auto-fill grid with 180px minimum tiles
- Responsive breakpoints: md (768px), lg (1024px)

## Component Design

### Landing Page Components

**Hero Section**:
- Height: 640px
- Background: Subtle gradient (light gray to white) with radial overlay accent
- Layout: 60/40 split - text left, image right
- Hero image: Modern smart home interface screenshot or lifestyle photo showing app in use
- CTA buttons: Primary blue with white text, generous padding (12px 24px)

**Feature Cards**:
- Background: White with subtle shadow (0 4px 12px rgba(0,0,0,0.06))
- Border: 1px solid light gray (#F1F5F9)
- Border radius: 12px (rounded-xl)
- Icon container: 48px square, light blue background (#E3F2FD), 12px radius
- Padding: 24px all sides
- Icons: 24px, primary blue color

**Client Logos Section**:
- Height: 120px
- Background: Light gray (#F5F7FA)
- Logos: Grayscale at 70% opacity, evenly spaced

**Testimonials**:
- Card-based layout with quotation styling
- Author photos: 48px circular avatars
- Background: White cards on light background

**CTA Section**:
- Height: 320px
- Background: Linear gradient (135deg, #1E88E5 to #1565C0)
- Text: White, centered
- Button: White background with blue text (inverted from primary)

**Footer**:
- Background: Dark (#0F1724)
- Text: White primary, gray secondary (#6B7280)
- 3-column grid (desktop): Logo/tagline, Quick Links, Newsletter
- Newsletter input: Dark background (#1a2332) with blue accent border

### Dashboard Components

**Header**:
- Fixed/sticky top navigation
- Logo left, settings/menu right
- Height: 64px
- Background: White with subtle bottom border

**Scene Pills**:
- Horizontal scrollable row
- Inactive: White background, subtle shadow
- Active: Primary blue background (#1E88E5), white text
- Border radius: 999px (fully rounded)
- Padding: 8px 12px
- Icons: Emoji-style for quick recognition (🏠 🚪 🌙)

**Room Pills**:
- Similar to scene pills but smaller
- Active state: Blue border instead of fill
- Horizontal scrollable on mobile

**Device Tiles**:
- Background: Linear gradient (white to very light blue #FBFDFF)
- Border: 1px solid #EEF2F7
- Border radius: 10px
- Padding: 12px
- Status chip: Light background (#F3F7FB), rounded pill shape
- Controls positioned at bottom of tile

**Device Controls**:
- Toggle buttons: Clear on/off states with color change
- Thermostat slider: 120px wide, range 16-30°C, 0.5° increments
- Temperature display: Adjacent to slider, bold weight

**Modal Dialogs**:
- Centered overlay with dark backdrop (rgba(12,18,30,0.45))
- Card: White background, 12px radius, max-width 520px
- Title: 20px, semibold
- Form controls: Consistent with design system

**Panels**:
- Background: White
- Shadow: 0 6px 18px rgba(15,23,36,0.04)
- Border radius: 12px
- Padding: 16px

## Interactive States

**Buttons**:
- Primary: Blue fill (#1E88E5), white text, hover: darker blue (#1565C0)
- Ghost: Transparent fill, border, hover: subtle background
- Focus: 3px blue outline with offset

**Cards**:
- Hover: Subtle scale (1.02) or shadow increase
- No hover on mobile/touch devices

**Form Inputs**:
- Background: Light gray (#F3F7FA)
- Border: Transparent default, blue on focus
- Border radius: 12px
- Padding: 10px 14px

## Animations
Use sparingly and purposefully:
- Scene transitions: Fade content change (300ms)
- Toast notifications: Slide in from bottom-right (200ms)
- Modal: Fade backdrop + scale modal (250ms)
- Device state changes: Instant feedback, no delay

## Images

**Hero Section**: 
- Large hero image showing the dashboard interface in use on a tablet/phone
- Alternative: Lifestyle photo of modern home with overlay of app interface
- Dimensions: Approximately 600x500px, right-aligned
- Style: High-quality, professional photography with soft lighting

**Features Section**:
- Icons only (no decorative images)
- Use Lucide React icon library for consistency

**Testimonials**:
- Customer avatars: 48px circular photos
- Real or stock photos showing diverse users

## Accessibility
- All interactive elements keyboard navigable
- ARIA labels on all buttons and controls
- Focus indicators: 3px outline, 2px offset
- Color contrast: WCAG AA minimum (4.5:1 for text)
- Screen reader announcements for state changes
- Touch targets: Minimum 44x44px

## Navigation Flow
Landing page links lead to dashboard:
- "Start Now" CTA → Dashboard (Room view)
- "Features" → Scrolls to features section
- Footer links → Respective landing page sections
- Dashboard "Home" icon → Returns to landing page