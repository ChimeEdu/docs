# Source: https://app.chimeedu.com/updates

CHANGELOG

# Updates & Changelog

Track what’s new and improved in ChimeEdu.

## Version 0.9.2

Codename: Daystrom

June 3, 2026

### AddedNew Features

- Platform Search — A new search experience across every classroom, activity, assessment, study guide, experience, student roster, and Knowledge Base article you own or have access to. Available three ways: a "hero" search bar on your Dashboard overview, a compact search in the top navigation on every other page, and a full /search results page with filtering by type, classroom refinement, and shortcuts to common "Create new …" actions
- Dashboard Hero Search — Type to see instant results grouped by content type, with quick-filter tabs (Classrooms, Activities, Learning Tools, Students, Actions, Help). Press Enter or click "View all results" to open the full results page
- Top-Nav Mini Search — A compact search input in the top navigation bar appears on every authenticated page outside your dashboard overview, so you can jump to any content from anywhere in the app
- Search Filters & Refinement — On the full /search page, narrow results by content type and by classroom, sorted by recency. Empty and no-results states surface quick "Create new …" shortcuts so you never hit a dead end
- Live Search Indexing — When you create, rename, or delete content, search results reflect the change within a few seconds — no manual reindex required

### ChangedImprovements

- Dashboard Welcome Layout — The greeting on your dashboard overview now reads as a single line ("Good afternoon, \[Name\]"), with the date line nestled just above. The animated welcome icon sits at the top, and there's more breathing room before your classrooms list
- Privacy Policy — Updated to disclose our new search infrastructure sub-processor (Algolia), the limited content metadata transmitted to power search, and the time-limited per-user access tokens that scope every search to only your own content
- Type Accent Colors — Search results, dashboard accent dots, and the Features mega menu now share one canonical color palette for each content type (classrooms coral, activities green, assessments yellow, study guides purple, experiences blue)
- Search Result Layout — Long titles and descriptions in search results now truncate cleanly with an ellipsis instead of wrapping or overflowing the card boundary

### FixedBug Fixes

- Student Search Results — A student enrolled in multiple of your classrooms now appears as a single result with all their classrooms listed, rather than once per enrollment
- Layout Overflow — Several listings (search results, dashboard activity cards) had a latent overflow bug under long titles. Result rows now stay inside their containers in every viewport
- General stability, accessibility, and security refinements

### SecuritySecurity & Privacy

- User-Scoped Search Access — Every search request is gated behind a per-user, time-limited (1-hour) signed access token issued by our backend. The underlying search API key is never delivered to the browser; the signed token cryptographically constrains each request to "only this user's content (plus public content like Knowledge Base articles)" at the search-infrastructure layer, so a tampered request cannot reach another user's data
- Content Sub-Processor — Search is powered by Algolia, a SOC 2 Type 2 certified search infrastructure provider. We transmit only the content metadata needed for search (titles, short descriptions, content type, classroom labels you've assigned, and timestamps). We do not transmit passwords, password hashes, authentication tokens, API keys, student grades, assessment submissions, or any personally identifying information beyond what a teacher already sees on their roster (name and email of the students they teach). Full disclosure in our updated Privacy Policy
- Audit Logging — Every search request is recorded with a per-user analytics token so administrators can investigate anomalies. The token is keyed to your account ID, not personal identifiers

## Version 0.9.1

Codename: Daystrom

April 29, 2026

### AddedNew Features

- Accessibility Conformance Report — New /accessibility page publishes our public VPAT 2.5 Rev WCAG report, with an animated Lighthouse Accessibility score (currently 100.0 / 100 averaged across our 10 public routes)
- Map Activity — Keyboard and on-screen-button controls for moving pins (Teacher Mode) and panning the map (all modes), as accessible alternatives to mouse-drag. Includes screen-reader announcements after each move
- Quick Activity creation — Step progress now announced to screen readers ("Step 2 of 4: Add Quiz Questions"), with a visible step indicator above the modal title
- Timeline PDF export — Server-side rendered with full PDF/UA-1 tagging. Resulting PDFs have selectable text, real heading structure, alt text on images, and document title in metadata. Replaces the previous image-only export
- Form autocomplete — Sign-up form now offers browser autofill for email, name, password, and organization fields

### ChangedImprovements

- Theme switcher — Consistent sun / moon / half-circle iconography across every theme menu on the platform (driven by your selected theme, not the time of day)
- Touch targets — Notification bell and per-notification delete controls enlarged to comfortably exceed the 24×24 CSS-pixel minimum
- Page titles — Browser tabs now show route-specific titles for every page (e.g. "ChimeEdu ∙ Classrooms") rather than inheriting a single platform-wide title
- Heading hierarchy — Document outline on every public page descends sequentially without skipped levels, improving screen-reader navigation
- Mobile keyboard hints — Code-entry inputs (join codes, invitation tokens, two-factor codes) now open the uppercase keyboard on iOS and Android by default

### FixedBug Fixes

- Theme menu — Visible label and assistive-technology announcement now stay in sync as you switch between Light / Dark / System
- Theme menu accessibility — Trigger now correctly links to its menu via aria-controls for assistive-technology users
- General stability and accessibility refinements

## Version 0.9.0

Codename: Daystrom

April 6, 2026

### AddedNew Features

- Fill-in-the-Blank Activity Type — Rich text editor for passage authoring with inline blanks, public player with auto-grading, hints, answer variants, and public landing page
- Invite-Only Registration — Closed Alpha registration gate with admin-managed invitations and branded invitation emails
- Dashboard Redesign — New layout with fixed navbar, push sidebar, sub-navigation pills, animated welcome component, and account drop-up menu
- Admin Overview Cards — Platform statistics dashboard for administrators
- Study Guide Video Blocks — YouTube and Vimeo embeds with local video upload support
- Experience Visibility Controls — Public sharing toggles for Travel and Google Drive file sections
- Sitemap & Robots.txt — SEO improvements for public pages and proper crawler directives
- Tier Change Email Notifications — Email notifications when account roles or tiers are updated

### ChangedImprovements

- Unified Activity Hero Cards — All activity types now share a single hero card layout on the dashboard
- Improved Rate Limiting — Tuned request limits and improved retry behavior for smoother multi-tab usage
- Email Templates — Redesigned transactional email templates with branded styling
- Modal Dialogs — Replaced browser-native confirm/prompt dialogs with custom modal components for better iPad compatibility
- Terms of Service & Privacy Policy — Updated to reflect all new activity types, invite-only registration, and expanded data collection disclosures

### FixedBug Fixes

- Fill-in-the-Blank Integration — Resolved field naming inconsistencies between frontend and backend
- Dashboard Spacing — Fixed layout regressions in hero grid and flex containers
- General stability and security improvements

## Version 0.8.0

Codename: Daystrom

March 17, 2026

### AddedNew Features

- iPad & Tablet Optimization - Safe area insets for notched devices, dynamic viewport height (100dvh) for iOS Safari, 44px touch targets per Apple HIG, and touch-friendly hover/focus states
- Google Drive Attachments on Public Study Guide Pages - Files & Resources section now visible on shared study guide links
- TipTap Link Input Redesign - Replaced browser prompt with inline URL input for iPad/tablet compatibility
- JSDoc Documentation - Comprehensive module-level documentation across all 72 backend files

### ChangedImprovements

- Responsive Card Grids - Added col-sm-6 intermediate breakpoint across 15+ pages for better two-column layouts on tablets
- Responsive Modals - Key modals now use modal-fullscreen-sm-down and modal-fullscreen-md-down for better mobile/tablet experience
- Experience Location Status - Backend is now single source of truth for location status computation
- Journal Entries Limit - Increased from 8 to 20 entries per journal entry
- Tablet Landscape Navbar - Slightly tighter padding to maximize content area
- Touch Interaction States - hover-lift, hover-slide-right, and hover-scale-center now have active/focus-visible equivalents on touch devices
- Focus Visibility - Improved outline styling with accent color for keyboard and touch navigation

### FixedBug Fixes

- Experience Status Buttons - Manual overrides (Arrive/Depart/Pending) now persist correctly instead of being overwritten by auto-computation
- Timezone-Aware Location Status - Fixed date handling in location status computation for correct timezone behavior
- Study Guide Public Page - Removed duplicate footer, fixed Table of Contents hidden behind navbar, fixed heading spacing not rendering due to CSS class placement
- Backend Cleanup - Removed debug logging from production code

## Version 0.7.2

Codename: Daystrom

February 25, 2026

### ChangedImprovements

- Map Activity exit behavior - Exiting Teacher or Student mode now returns to the view-mode URL (/map/\[id\]?mode=view) instead of leaving users on the defunct /map/\[id\] path
- Map Activity Preview mode - Top navbar is now hidden in Preview mode (consistent with view, teacher, and student modes)
- Map Activity layout - Zoom level changes no longer push the header bar upward; layout uses flex and overflow containment for a stable full-screen experience
- Map Activity pin modals - Images section is always shown for non-temporary pins; supports filepath, filePath, and image\_url for thumbnails; thumbnails open in fslightbox when clicked

### FixedBug Fixes

- Map Activity pin view modal - Fixed crash when opening a pin (TypeError on missing image filepath); added defensive checks for pin images in view modal and lightbox
- Map Activity View mode images - Pin image thumbnails now appear correctly in View mode for both public and authenticated users

## Version 0.7.1

Codename: Daystrom

January 20, 2026

### AddedNew Features

- Map Activity Landing Page - Public landing page for map activities with activity details and mode selection
- Feature Pages - Individual marketing pages for each activity type (Classrooms, Maps, Quizzes, Assessments, Flash Cards, Timelines, Study Guides)
- Feature Page Mock-ups - Visual mock-ups for each feature page showcasing activity functionality
- Footer Reorganization - New Features column with improved link organization
- Homepage Feature Cards - Enhanced feature cards with visual mock-ups and improved styling

### ChangedImprovements

- Enhanced Map Activity Routing - Map activities now route to landing page when no mode is specified
- Improved Footer Layout - All columns now use consistent 20% width with reordered columns
- Updated Feature Page Layouts - Consistent hero sections with two-column layouts and scaled mock-ups
- Enhanced Classrooms Feature Page - Added icon box to title section and new two-card section at bottom
- Enhanced Assessments Feature Page - Added navigation buttons, larger textarea, and improved spacing
- Improved Footer Status Link - Added external icon indicator for Status page link

### FixedBug Fixes

- Map Activity Public Access - Fixed map activities to show landing page for logged-out users
- Map Activity Google Drive Attachments - Google Drive attachments now visible on public map activity pages
- Feature Page Vertical Alignment - Fixed mock-up vertical alignment on Classrooms, Quizzes, and Assessments pages
- Footer Column Ordering - Reordered columns for better logical flow

## Version 0.7.0

Codename: Daystrom

January 19, 2026

### AddedNew Features

- Timeline Activity Type - Complete implementation with event management and chronological visualization
- Timeline Editor - Full offcanvas editor with event creation, editing, and drag-and-drop reordering
- Timeline Player - Interactive timeline view with horizontal and vertical orientations
- Timeline Play Mode - Auto-progression animation with speed control, looping, and event card expansion
- Timeline Mini-Cards - Compact event cards with thumbnail images, dates, and titles
- Timeline Event Modals - Full event details with featured images, location maps, and rich text descriptions
- Timeline Settings - Orientation modes (horizontal/vertical), access controls, and animation settings
- Timeline Export - PDF and image export functionality for timeline activities
- Location Integration - Leaflet map picker for event locations with map preview in modals
- Timeline Landing Page - Stylized timeline visualization with mock event cards
- Google Drive Integration for Timelines - Attach files and folders to timeline activities
- Timeline Search and Filter - Search events by title/description and filter by date range
- Timeline Navigation Controls - Forward/backward and up/down controls for timeline navigation
- Timeline Progress Indicator - Visual progress tracking for timeline playback
- Platform Event Tracking - Key user actions tracked via Cronitor for performance monitoring
- Support Page Redesign - Updated layout with Knowledge Base, Email Us, and Platform Status cards using Columns with Icons style

### ChangedImprovements

- Enhanced Activity Creation Workflow - Added Timeline as new activity type option
- Improved Activity Dashboard - Timeline-specific dashboard with event overview and management
- Updated Activity Landing Pages - Timeline landing page with unique timeline visualization
- Enhanced Editor Workflow - Consistent offcanvas editor pattern for Timelines
- Improved Google Drive Integration - Extended to support Timeline activities
- Updated Support Page Layout - Left-justified card contents with full-width CTAs
- Enhanced Timeline Navigation - Back button now navigates to associated classroom when available
- Improved Timeline Layout - Consistent horizontal and vertical orientations with proper card alignment
- Updated Privacy Policy and Terms of Service - Added Cronitor.io RUM and custom event tracking information

### FixedBug Fixes

- Resolved timeline event positioning and spacing issues
- Fixed timeline card alignment and connector placement
- Improved timeline scrolling and overflow handling
- Enhanced timeline play mode auto-scrolling for expanded cards
- Fixed timeline modal padding and layout consistency
- Resolved timeline orientation switching issues
- Improved timeline search field positioning and alignment

## Version 0.6.1

Codename: Daystrom

January 18, 2026

### AddedNew Features

- Homepage Feature Cards Redesign - White title containers with colored icon boxes and arrow links
- Feature Cards Icon Boxes - Colored frames for activity type icons with improved spacing
- Feature Cards Arrow Links - Interactive arrow icons with hover animations for future feature pages
- Homepage Section Title Update - Changed to "Meaningful tools for Interactive Learning"

### ChangedImprovements

- Enhanced Homepage Feature Cards - Updated layout with white title containers and improved visual hierarchy
- Improved Feature Card Icons - Icons now in colored boxes with better padding and sizing
- Updated Feature Card Styling - Refined spacing, padding, and hover interactions
- Improved Activity Icon Display - Fixed Flash Card icon display on Dashboard and Activities pages

### FixedBug Fixes

- Flash Card Icon Display - Corrected icon display for Flash Card activities on Dashboard and Activities pages
- Activity Type Icon Logic - Updated icon selection logic to properly handle Flash Card activity type
- Sidebar Account Menu Positioning - Fixed account drop-up menu to remain locked to bottom of sidebar

## Version 0.6.0

Codename: Daystrom

January 17, 2026

### AddedNew Features

- Flash Card Activity Type - Complete implementation with deck and card management
- Flash Card Editor - Full offcanvas editor with deck creation, card creation, and drag-and-drop reordering
- Flash Card Player - Interactive study interface with Flip, Type Answer, and Multiple Choice modes
- Spaced Repetition Algorithm - SM-2 algorithm for intelligent card review scheduling
- Flash Card Landing Page - Stylized card stack visualization with hover animations
- Google Drive Integration for Flash Cards - Attach files and folders to flashcard activities
- Flash Card Preview Mode - Teachers can preview flashcard activities before student access
- Rich Text Support for Cards - Full TipTap editor for front and back card content
- Image Upload for Cards - Support for images on both front and back of cards
- Card Progress Tracking - Individual progress tracking per card with spaced repetition intervals
- Deck Management - Create, edit, delete, and reorder flashcard decks
- Card Management - Create, edit, delete, and reorder cards within decks

### ChangedImprovements

- Enhanced Activity Creation Workflow - Added Flash Card as new activity type option
- Improved Activity Dashboard - Flash Card-specific dashboard with deck and card overview
- Updated Activity Landing Pages - Flash Card landing page with unique card stack visualization
- Enhanced Editor Workflow - Consistent offcanvas editor pattern for Flash Cards
- Improved Google Drive Integration - Extended to support Flash Card activities

### FixedBug Fixes

- Resolved card deletion parameter mismatch - Fixed incorrect API call parameters for card deletion
- Fixed card update parameter mismatch - Corrected API call parameters for card updates
- Improved card ID handling - Ensured correct card IDs are passed to backend operations
- Enhanced error handling for flashcard operations - Better error messages and validation

## Version 0.5.1

Codename: Daystrom

January 16, 2026

### AddedNew Features

- Platform Notifications Composer - Admin tool for sending on-platform notifications to users
- Icon Picker for Platform Notifications - Comprehensive icon selection with 40+ Bootstrap icons
- Expanded Notification System - Account security notifications (password changes, 2FA, passkeys, new device sign-ins)
- Account change notifications - Automatic alerts when account type/tier is modified
- Notification deletion functionality - Delete individual notifications from bell menu and Notifications page
- Mark All as Read functionality - Bulk mark notifications as read on Notifications page
- Notification hover states - Visual feedback when hovering over notifications
- Limited notification display - Show 4 most recent notifications in bell menu before overflow

### ChangedImprovements

- Enhanced Platform Notifications - Separated from email system, now exclusively on-platform
- Improved notification icon display - Icons now white in dark mode for better visibility
- Updated Emails & Messaging section - Added Platform Notifications tab with composer interface
- Enhanced notification bell menu - Improved layout with delete buttons and hover states
- Improved Notifications page - Card-based layout with rounded borders and better visual hierarchy

### FixedBug Fixes

- Resolved blank icons in icon picker - Removed duplicate icon entries
- Fixed notification icon colors in dark mode - Icons now display white instead of blue
- Improved notification spacing - Removed extra gap before notification titles
- Enhanced notification borders - All sides now have rounded borders on Notifications page

## Version 0.5.0

Codename: Daystrom

January 15, 2026

### AddedNew Features

- Assessment Notifications System - Email and on-platform notifications for assessment submissions
- Notification Bell in Navbar with unread count badge
- Full Notifications Page with filtering (All/Unread) and management
- Notification Preferences in Account Settings
- Real-time notification updates and mark-as-read functionality
- Database-backed notification system with user preferences

### ChangedImprovements

- Enhanced assessment submission workflow with automatic teacher notifications
- Improved teacher workflow with instant submission alerts
- Updated Navbar with notification bell for quick access
- Enhanced Account Settings with notification preferences section

### FixedBug Fixes

- Improved teacher awareness of student assessment submissions
- Enhanced notification delivery reliability

## Version 0.4.3

Codename: Daystrom

January 14, 2026

### AddedNew Features

- Assessment Preview Mode - Teachers can perform dry runs of assessments without creating submissions
- Assessment Landing Page with modern layout matching Activity Landing Pages
- Assessment Dashboard with offcanvas editors for Questions and Settings
- Google Drive integration for Assessment attachments
- Theme Switcher in Assessment Player page
- Image Select question type with square aspect ratio (1:1) and viewport-based sizing
- Enhanced Assessment Editor with Featured Image, Icon Picker, and Google Drive management

### ChangedImprovements

- Reorganized Assessment Dashboard layout - Files & Folders moved below Overview, Questions and Share side-by-side
- Submissions section expanded to full width
- Assessment Player page updated with Preview Mode banner (Bootstrap-compliant warning alert)
- Image Select questions now display images in 1:1 aspect ratio with max 20vh sizing
- Preview Mode alert positioned at bottom with 2em spacing, using Bootstrap warning alert styling

### FixedBug Fixes

- Resolved Assessment Editor saving issues - Featured Images, Classroom linking, and Settings now persist correctly
- Fixed Google Drive attachment linking for Assessments (database column type migration)
- Corrected FormData parsing for Assessment updates (settings, classroom\_ids, expected\_submissions)
- Fixed Assessment creation with alphanumeric ID system
- Resolved password handling for Assessments (NOT NULL constraint)
- Improved Assessment Dashboard state refresh after saving changes

## Version 0.4.2

Codename: Daystrom

January 17, 2025

### AddedNew Features

- Alphanumeric ID system for activities and assessments (6-character IDs for activities, A- prefix for assessments)
- Map Settings offcanvas for configuring map backgrounds (SVG, Leaflet location)
- Enhanced sidebar with bottom-weighted Account drop-up menu
- Improved flexbox layout for sidebar navigation

### ChangedImprovements

- Migrated activity and assessment primary keys from integer to alphanumeric format
- Updated all public routes to use activity IDs instead of slugs
- Improved Account section positioning in sidebar
- Enhanced Map Activity Dashboard with Map Settings integration
- Updated ID validation and normalization across all routes

### FixedBug Fixes

- Resolved Account section positioning issues in sidebar
- Fixed activity creation with new alphanumeric ID system
- Corrected map and pin loading with new ID format
- Resolved Google Drive attachment linking after ID migration
- Fixed QR code generation for Quiz Activities with new IDs
- Improved navbar visibility logic for alphanumeric route patterns

## Version 0.4.1

Codename: Daystrom

January 16, 2025

### AddedNew Features

- Activity Landing Pages for Map and Quiz activities
- Featured image and icon support for activities
- Enhanced Map Activity Dashboard with Pins management
- Offcanvas editor for Map Activities with improved layout
- Share card with QR code and email sharing functionality
- Bootstrap List Groups for pins display with creation dates

### ChangedImprovements

- Replaced legacy Map Editor page with streamlined Dashboard
- Updated Map Activity editor from modal to offcanvas
- Improved icon picker with 28 icons in collapsible component
- Enhanced password fields with show/hide toggles
- Updated Dashboard layout for better organization
- Improved Google Drive attachment management in Activity editor

### FixedBug Fixes

- Resolved navbar visibility issues in Map Activity modes
- Fixed public access for Map Activity View mode
- Improved Activity editor state management
- Enhanced pin list display with proper Bootstrap styling

## Version 0.4.0

Codename: Daystrom

January 15, 2025

### AddedNew Features

- Enhanced Google Drive integration with file and folder support
- Drag-and-drop file reordering for classroom attachments
- Automatic file name synchronization with Google Drive
- Advanced email template system with split-view editor
- Email composition tool for batch messaging
- Improved sidebar navigation with user menu at bottom
- Enhanced email template responsiveness and design options

### ChangedImprovements

- Improved Google Drive picker interface and file selection
- Enhanced email template rendering with better mobile support
- Updated sidebar layout for better user experience
- Improved email composition workflow for administrators
- Enhanced file attachment display on public classroom pages

### FixedBug Fixes

- Resolved Google Drive picker display and positioning issues
- Fixed file name display for Google Drive attachments
- Improved folder selection in Google Drive integration
- Enhanced email template variable handling

## Version 0.3.4

Codename: Daystrom

January 10, 2025

### AddedNew Features

- Elaborate gradient backgrounds for hero sections across all sub-pages
- Enhanced homepage hero with matching gradient effects
- Improved visual consistency across platform pages

### ChangedImprovements

- Updated hero section styling with multi-layered gradient effects
- Standardized page title fonts and sizing across all pages
- Enhanced subtitle styling with improved font weights
- Improved gradient transitions for smoother visual flow
- Better color blob distribution in homepage hero
- Refined spacing and layout in hero containers

### FixedBug Fixes

- Improved gradient coverage and blending across hero sections
- Enhanced dark mode gradient support

## Version 0.3.3

Codename: Daystrom

January 9, 2025

### AddedNew Features

- New user tiers: Plus and Premium with expanded limits
- Two-Factor Authentication (2FA) and Passkey support
- Contact form and issue reporting system
- Form submissions management for admins
- New pages: Support, Features, FAQs, Pricing, About Us, Terms of Service, Changelog
- Print-friendly view and share functionality for Knowledge Base articles
- Email confirmation workflow for new user registrations
- Scroll-to-top functionality on route changes

### ChangedImprovements

- Enhanced registration workflow with email confirmation
- Improved password requirements (minimum 10 characters with complexity)
- Enhanced email templates with brand-friendly design
- Better dark mode support across all pages
- Improved breadcrumb styling and navigation
- Updated favicon support across all subdomains
- Mobile optimization for homepage
- Map Activity rebuild with unified components
- Admin Dashboard upload management improvements

### FixedBug Fixes

- Resolved display issues with conditional elements
- Fixed navbar overlap on article pages
- Corrected image upload handling for articles
- Resolved various UI and performance issues

## Version 0.3.2

Codename: Daystrom

January 5, 2025

### AddedNew Features

- Enhanced platform documentation
- Improved system reliability and performance

### ChangedImprovements

- Major codebase cleanup and organization
- Improved system architecture and infrastructure
- Enhanced platform stability and efficiency

### RemovedDeprecated Features

- Deprecated features and legacy code
- Unused components and outdated functionality
- Help button from Navbar (replaced with improved help system)

## Version 0.3.1

Codename: Daystrom

January 3, 2025

### AddedNew Features

- Page management for Map Activity pins
- Enhanced integration capabilities

### ChangedImprovements

- Footer redesign with improved navigation
- Homepage hero redesign for logged-in users
- Badge styling updates (Dark Mode compatible)
- Improved platform workflow and processes
- Enhanced assessment submission management

### FixedBug Fixes

- Assessment feature complete with all QOL improvements

## Version 0.3.0

Codename: Daystrom

December 20, 2024

### AddedNew Features

- Complete Map Activity rebuild with improved functionality
- Page management system for permanent map activities
- Enhanced page type support for richer content
- Improved image viewing experience
- Required student password for temporary map activities

### ChangedImprovements

- Immediate pin content updates
- Improved content organization and display
- Safe page reordering with validation
- Enhanced map rendering performance

Want to stay updated? Check back regularly or follow us for announcements.

Have questions about an update? [Contact us](https://app.chimeedu.com/contact) or visit our [Support page](https://app.chimeedu.com/support).