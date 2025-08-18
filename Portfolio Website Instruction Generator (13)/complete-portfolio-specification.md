# Arshaan Khan Portfolio - Complete Technical Specification

## GLOBAL DESIGN SYSTEM

### Color Variables (CSS Custom Properties)
**Light Theme (Default):**
- `--background`: #F9F8F6 (Cream background)
- `--foreground`: #000000 (Black text)
- `--secondary`: #E9EBE9 (Light gray secondary)
- `--border`: #000000 (Black borders)
- `--chart-1`: #5C54F9 (Primary purple)
- `--chart-2`: #4D20FF (Deep purple)
- `--chart-3`: #E46289 (Pink)
- `--chart-4`: #FF5789 (Coral)
- `--chart-5`: #1CF2CC (Mint green)

**Dark Theme (.dark class):**
- `--background`: #000000 (Black background)
- `--foreground`: #F9F8F6 (Cream text)
- `--secondary`: #1A1A1A (Dark gray secondary)
- `--border`: #F9F8F6 (Cream borders)

### Typography System
- **Font Family**: Inter, -apple-system, BlinkMacSystemFont, Segoe UI, Roboto
- **Base Font Size**: 14px
- **Letter Spacing**: -0.05em globally
- **Font Weights**: Normal (400), Medium (500), Semibold (600), Bold (700)

### Layout System
- **Max Container Width**: 1800px (max-w-[1800px])
- **Horizontal Padding**: 40px (px-10)
- **Border Radius**: 30px for large elements, 50px for circular buttons
- **Smooth Scrolling**: Enabled globally

---

## 1. HEADER COMPONENT

### Structure & Positioning
- **Position**: Fixed, full width, z-index 50
- **Top Bar**: 10px height (h-2.5), background color bar
- **Container**: Max-width 1800px, centered, 40px horizontal padding

### Logo Section
- **Dimensions**: 200px width × 64px height (w-[200px] h-16)
- **Background**: Foreground color (inverts with theme)
- **Border Radius**: 8px (rounded-lg)
- **Text**: "Arshaan Khan" - 20px bold font (text-xl font-bold)
- **Text Color**: Background color (text-background)
- **Container**: Auto width, 64px height, 30px bottom radius, 12px right margin

### Corner Decorations (SVG)
- **Dimensions**: 30px × 30px each
- **Position**: Absolute positioned at corners
- **Path**: Curved corner transitions (d="M30 0H0V30C0 13.431 13.431 0 30 0Z")
- **Color**: Background color (fill="currentColor" className="text-background")

### Desktop Navigation
- **Background**: Semi-transparent white (bg-white/50) with 10px blur (backdrop-blur-[10px])
- **Dimensions**: 58px height, 50px border radius
- **Border**: 1px gray border with 50% opacity, shadow
- **Margin**: 10px top (mt-2.5)
- **Menu Items**: "Projects", "About", "Blog", "Contact"
- **Link Styling**: 14px padding horizontal, 8px vertical, 16px font, hover opacity 70%

### Theme Toggle Button
- **Dimensions**: 40px × 40px (w-10 h-10)
- **Border**: 1px foreground color, 35px border radius
- **Icon Container**: 20px × 20px (w-5 h-5) with conditional styling
- **Dark Mode**: Shadow inset effect, 50% scale
- **Light Mode**: Different shadow, 100% scale, -2deg rotation
- **Animation**: 300ms transition on all properties

### Mobile Menu Toggle
- **Dimensions**: 80px × 40px (w-20 h-10)
- **Border**: 2px foreground, 20px radius
- **Text**: "Menu" with medium font weight
- **Margin**: 8px left from logo

### Mobile Menu Overlay
- **Background**: #5C54F9 (purple)
- **Dimensions**: Full width, 80vh height, max 540px height
- **Border Radius**: 30px_0_30px_30px (custom corners)
- **Padding**: 32px (p-8)
- **Text Color**: White
- **Menu Items**: 32px font size (text-2xl), white border bottom, 4px padding bottom, 4px margin bottom
- **Theme Toggle Position**: Absolute bottom 16px, white border, 50px radius, 15px height

---

## 2. HERO SECTION

### Layout Structure
- **Container**: Max-width 1800px, 40px padding, 10px top margin
- **Main Layout**: Flex justify-between, 10px gap
- **Height**: 95vh with 630px minimum
- **Structure**: Large left section + narrow right column (280px)

### Left Section - Main Hero Content
- **Background**: Animated canvas gradient (463px × 855px)
- **Border Radius**: 30px on all corners
- **Canvas Filter**: hue-rotate(330deg)

#### Gradient Animation Specifications
- **Canvas Size**: 463px × 855px
- **Animation**: Radial gradient with sine/cosine movement
- **Center Point**: 200 + sin(frame * 0.01) * 50, 400 + cos(frame * 0.01) * 50
- **Inner Radius**: 50px
- **Outer Radius**: 300px
- **Color Stops**:
  - 0: #5C54F9 (Purple)
  - 0.3: #4D20FF (Deep purple)
  - 0.6: #E46289 (Pink)
  - 1: #FF5789 (Coral)

#### Noise Overlay
- **Pattern**: SVG-based turbulence filter with 40% opacity
- **Coverage**: Full canvas area with 30px border radius

#### Content Text Box
- **Position**: Bottom-right of left section
- **Dimensions**: 50% max width, 250px height
- **Background**: Theme background color
- **Shape**: Rounded top-right (30px), square other corners
- **Padding**: 20px all sides, 0 bottom

#### Hero Text Specifications
- **Font Size**: Responsive clamp(2.35rem, 2.114rem+1vw, 3.75rem)
- **Max Width**: 20 characters per line (max-w-[20ch])
- **Line Height**: 1.1
- **Content**: "AI Automater, Business Analyst & Web Designer"
- **Color**: Foreground

#### Scroll Button
- **Dimensions**: 50px × 50px circular (w-[50px] min-h-[50px])
- **Border**: 2px foreground color, 50px radius
- **Margin**: 4px bottom
- **Icon**: 20px arrow (w-5 h-5), 90deg rotation
- **Hover Effects**: 110% scale, additional 20deg rotation
- **Link**: Smooth scroll to #about section

### Right Column - Stats & Blog (280px width)

#### Statistics Carousel
- **Shape**: Perfect circle, 280px diameter (w-[280px] aspect-square)
- **Border**: 2px foreground color, full radius
- **Background**: Theme background
- **Content**: Auto-playing carousel with 5 statistics

#### Stat Card Content
- **Number Font**: 64px normal weight (text-[4rem])
- **Description Font**: 16px base, 70% opacity, max 15 characters width
- **Layout**: Centered column flex, 32px padding
- **Data Points**:
  - "50+" - AI automation solutions deployed
  - "200K" - Hours saved through automation  
  - "15+" - Business processes optimized
  - "95%" - Client satisfaction rate
  - "3" - Years of AI expertise

#### Blog Carousel
- **Dimensions**: 280px width × remaining height
- **Background**: #5C54F9 (purple)
- **Border Radius**: 30px
- **Content**: Auto-playing carousel with 5 blog posts

#### Blog Card Content
- **Image Container**: 280px × 150px, 20px border radius, white/10% background
- **Text Font**: 25.6px normal weight (text-[1.6rem]), white color
- **Text Width**: 15 characters maximum (w-[15ch])
- **Padding**: 16px all sides

#### Blog Data Array
1. **"Creating Creative Creations🧬🤖"** - Robot image (imported asset)
2. **"Data-driven insights: transforming business analytics."** - Placeholder image
3. **"Modern web design trends for 2025."** - Placeholder image
4. **"AI integration strategies for small businesses."** - Placeholder image
5. **"The future of business process automation."** - Placeholder image

#### Navigation Button (Blog Section)
- **Position**: Absolute bottom-right corner
- **Outer Container**: 60px square, 35px top-left radius
- **Inner Button**: 50px circle, 2px border, background color
- **Margins**: 4px right, 4px bottom
- **Icon**: 20px arrow with hover effects (110% scale, -20deg rotation)

---

## 3. PROJECTS SECTION

### Section Layout
- **Container**: Max-width 1800px, 40px padding, 80px top margin
- **Header**: "SELECTED WORK" - 19.2px light font, 0.5px letter spacing, uppercase, 50% opacity, 64px bottom margin

### Project Layout Structure
- **Project Container**: Full width, 64px gap between projects, 80px vertical spacing
- **Layout Pattern**: Alternating left-right (flex-row-reverse for odd indices)
- **Item Structure**: 50% image + 50% content with 64px gap

### Project Image Container
- **Dimensions**: 50% width, 400px height
- **Border Radius**: 30px
- **Background**: Secondary color
- **Hover Effect**: 102% scale with 500ms duration

### Status Badge
- **Position**: Absolute top-left, 24px margins
- **Padding**: 16px horizontal, 8px vertical
- **Border Radius**: Full (50px)
- **Colors**: Green background (#10B981) + white text for "Live"

### Hover Overlay
- **Background**: Black with 20% opacity
- **Animation**: Opacity 0 to 100% on group hover, 300ms duration

### Project Content Structure
- **Width**: 50% of container
- **Layout**: Flex column

#### Category Label
- **Font**: 14.4px light weight (text-[0.9rem] font-light)
- **Letter Spacing**: 1px
- **Transform**: Uppercase
- **Color**: #5C54F9 (purple)
- **Margin**: 12px bottom
- **Opacity**: 70%

#### Project Title
- **Font**: 64px normal weight (text-[4rem])
- **Line Height**: 1
- **Letter Spacing**: -2px
- **Margin**: 16px bottom
- **Hover Color**: #5C54F9 with 300ms transition

#### Description Text
- **Font**: 18px relaxed line height
- **Color**: Foreground with 80% opacity
- **Max Width**: 25 characters (max-w-[25ch])
- **Margin**: 24px bottom

#### Technology Tags
- **Layout**: Flex wrap with 8px gaps
- **Each Tag Styling**:
  - Padding: 12px horizontal, 4px vertical
  - Background: Secondary color
  - Border: 1px border color
  - Border Radius: Full (50px)
  - Font: 14px

#### View Project Button
- **Layout**: Inline flex with 12px gap
- **Text**: "View Project" - 18px medium font
- **Icon Container**: 48px diameter circle, 2px current color border
- **Icon**: 20px arrow (w-5 h-5)
- **Hover Effects**:
  - Text color: #5C54F9
  - Icon scale: 110%
  - Icon rotation: -20 degrees

### Project Data Array
1. **Neurion AI**
   - Category: "AI Automation Platform"
   - Description: "Advanced neural network platform for business automation and intelligent decision-making systems."
   - Link: https://neurionai.netlify.app/
   - Technologies: ["Python", "TensorFlow", "React", "FastAPI"]
   - Status: "Live"

2. **AI Doctor**
   - Category: "Healthcare AI Solution"
   - Description: "Intelligent medical diagnosis system using machine learning to assist healthcare professionals."
   - Link: https://github.com/arsh44n/AI-Voice-Prescription
   - Technologies: ["AI/ML", "Python", "React", "PostgreSQL"]
   - Status: "Live"

3. **HR Analytics**
   - Category: "Business Intelligence"
   - Description: "Comprehensive analytics dashboard for human resources performance tracking and insights."
   - Link: https://github.com/arsh44n/HR-insight-Analytics
   - Technologies: ["Power BI", "SQL", "Python", "React"]
   - Status: "Live"

### View All Projects Link
- **Position**: Center bottom, 80px top margin
- **Text**: "View All Projects" - 20px medium font
- **Icon**: 56px diameter circle, 2px border
- **Icon Size**: 24px (w-6 h-6)
- **Link**: https://github.com/arsh44n
- **Hover**: 110% scale, -20deg rotation, purple color

---

## 4. ABOUT SECTION

### Section Layout
- **Container**: Max-width 1800px, 40px padding
- **Spacing**: 96px vertical margins, overflow-x hidden
- **Layout**: Two-column flex with 64px gap

### Profile Image
- **Dimensions**: 400px max width, 300px min width, 500px height
- **Border Radius**: 30px
- **Background**: Secondary color fallback
- **Image**: Imported anime-style portrait (figma:asset)

### Text Content Section

#### Main Description
- **Font**: 35.2px light weight (text-[2.2rem] font-light)
- **Line Height**: 1.4
- **Max Width**: 28 characters per line (max-w-[28ch])
- **Min Width**: 20 characters (min-w-[20ch])
- **Margin**: 24px bottom
- **Bold Spans**: "I'm Arshaan Khan", "intelligent technology solutions"

#### Secondary Description
- **Font**: 18px relaxed line height
- **Color**: Foreground 80% opacity
- **Max Width**: 35 characters
- **Margin**: 24px vertical

#### Core Expertise Section
- **Header**: "Core Expertise:" - 20px medium font, 16px bottom margin
- **Layout**: 2-column grid, 16px gaps, 400px max width

#### Expertise Items
- **Dot**: 8px diameter purple circle (#5C54F9)
- **Text**: Foreground 80% opacity
- **Items**: "AI Automation", "Business Analysis", "Web Design", "Data Analytics"

#### Contact Button
- **Padding**: 8px vertical, 16px horizontal
- **Border**: 2px foreground, 50px radius
- **Font**: 28.8px normal weight (text-[1.8rem])
- **Background**: Transparent, hover fills with foreground
- **Text**: "✦ Get in touch ✦"
- **Stars**: Spinning animation (2s duration, 4s delay)
- **Link**: Smooth scroll to #contact

---

## 5. SKILLS SECTION

### Section Layout
- **Container**: Max-width 1800px, 40px padding, 160px vertical margin
- **Header**: "SKILLS & EXPERTISE" - Same styling as projects header

### Skills Showcase Layout
- **Structure**: Vertical stack, 80px gaps between items
- **Container**: Centered flex column, 128px bottom margin

#### Each Skill Item Structure
- **Layout**: Horizontal flex with group hover effects
- **Font**: 112px semibold (text-[7rem] font-semibold)
- **Responsive**: 96px (md), 80px (lg), 64px (xl), 112px (2xl)
- **Letter Spacing**: -0.05em
- **Text Color**: Foreground

#### Expandable Image Container
- **Default State**: 0 width, transparent border, 16px horizontal margin
- **Hover State**: 192px width (w-[12rem]), foreground border (2px)
- **Animation**: 500ms ease-in-out transition
- **Border Radius**: 30px

#### Image Scaling
- **Default**: Scale 0, 500ms transition
- **Hover**: Scale 100%
- **Dimensions**: 192px × 192px with cover fit
- **Background**: Secondary color

#### Skills Data Array
1. **["AI", "automation"]** - AI technology image from Unsplash
2. **["Business", "analysis"]** - Business charts image
3. **["Web", "design"]** - Code/development image  
4. **["Data", "analytics"]** - Data visualization image
5. **["Process", "optimization"]** - Engineering/systems image

### Services Grid Section
- **Header**: "SERVICES OFFERED" - Centered, same header styling
- **Layout**: 3-column grid (responsive to 1-column on mobile)
- **Gap**: 32px between cards

#### Service Card Styling
- **Background**: Secondary color
- **Border Radius**: 30px
- **Padding**: 32px
- **Border**: 1px border color, changes to purple (#5C54F9) on hover
- **Hover Effects**: 102% scale, purple border

#### Card Content Structure
- **Title**: 24px medium font, changes to purple on hover
- **Description**: Foreground 80% opacity, relaxed line height, 24px bottom margin
- **Feature List**: 8px vertical spacing

#### Feature List Items
- **Dot**: 6px purple circle (#5C54F9)
- **Text**: Foreground 70% opacity
- **Gap**: 8px between dot and text

#### Hover Indicator
- **Container**: 32px circle, 2px purple border
- **Icon**: 16px arrow, purple color
- **Animation**: Opacity 0 to 100% on card hover

#### Services Data Array
1. **AI Automation Solutions**
   - Description: "Custom AI-powered automation systems that streamline business processes and reduce manual workload."
   - Features: ["Workflow Automation", "Intelligent Decision Making", "Process Optimization", "AI Integration"]

2. **Business Analysis & Consulting**
   - Description: "Strategic business analysis to identify opportunities, optimize operations, and drive growth."
   - Features: ["Requirements Analysis", "Process Mapping", "Performance Metrics", "Strategic Planning"]

3. **Web Design & Development**
   - Description: "Modern, responsive web applications built with cutting-edge technologies and user-centric design."
   - Features: ["Custom Web Apps", "Responsive Design", "User Experience", "Performance Optimization"]

---

## 6. CONTACT SECTION

### Main Contact Area
- **Container**: Max-width 1800px, 40px padding, 32px top margin
- **Dimensions**: Full width, 700px height
- **Border Radius**: 30px
- **Padding**: 80px (p-20)
- **Margin**: 32px bottom

### Background Animation
- **Canvas Size**: 1600px × 1000px
- **Effects**: 10px blur, 110% scale
- **Position**: Absolute, full coverage

#### Gradient Animation Specifications
- **Center Movement**: 800 + sin(frame * 0.005) * 200, 500 + cos(frame * 0.003) * 150
- **Radii**: Inner 100px, Outer 600px
- **Color Stops**:
  - 0: #5C54F9 (Purple)
  - 0.2: #4D20FF (Deep purple)
  - 0.5: #E46289 (Pink)
  - 0.8: #FF5789 (Coral)
  - 1: #1CF2CC (Mint green)

### Noise Overlay
- **Pattern**: Same SVG turbulence as hero section
- **Opacity**: 40%
- **Border Radius**: 30px

### Content Layout
- **Structure**: Flex column, space-between, full height
- **Z-index**: 2 (above background)

#### Main Headline
- **Font**: 96px normal weight (text-[6rem])
- **Responsive**: 48px (md), 64px (lg), 80px (xl), 96px (2xl)
- **Color**: White
- **Line Height**: 1.1em
- **Max Width**: 12 characters (max-w-[12ch])
- **Content**: "Ready to transform your business with **AI automation?**"
- **Bold Text**: "AI automation" with font-bold

#### Subtext
- **Font**: 20px (text-xl)
- **Color**: White 80% opacity
- **Max Width**: 30 characters
- **Line Height**: Relaxed
- **Content**: "Let's discuss how AI automation and business analysis can streamline your operations and drive growth."

#### Call-to-Action Button
- **Padding**: 12px vertical, 24px horizontal
- **Border**: 2px white, 50px radius
- **Font**: 28.8px normal weight (text-[1.8rem])
- **Background**: Transparent, hover fills white
- **Text Color**: White, hover black
- **Content**: "✦ Let's collaborate ✦"
- **Stars**: Spinning animation (2s duration, 4s delay)
- **Link**: mailto:arsh44n.work@gmail.com

#### Email Section
- **Font**: 22.4px light weight (text-[1.4rem])
- **Color**: White
- **Margin**: 24px bottom
- **Email Link**: arsh44n.work@gmail.com with hover underline

#### Social Links Container
- **Layout**: Horizontal flex, 16px gaps
- **Position**: Self-end on desktop, centered on mobile

#### Social Link Buttons
- **Dimensions**: 48px × 48px circles (w-12 h-12)
- **Border**: 2px white, full radius
- **Icons**: 24px size (w-6 h-6)
- **Hover**: White background, black icons
- **Links**:
  - **LinkedIn**: https://www.linkedin.com/in/arsh44n
  - **GitHub**: https://github.com/arsh44n
  - **Email**: mailto:arsh44n.work@gmail.com

### Footer Section
- **Padding**: 32px vertical (py-8)
- **Border**: Top border with border color
- **Layout**: Space-between flex
- **Text Color**: Foreground 60% opacity
- **Left Text**: "© 2025 Arshaan Khan. All rights reserved."
- **Right Text**: "AI Automater • Business Analyst • Web Designer"

---

## TECHNICAL SPECIFICATIONS

### Animation System
- **Smooth Scrolling**: Enabled globally via CSS
- **Carousel Auto-play**: Infinite loop, 3-second intervals
- **Hover Transitions**: 300-500ms ease timing functions
- **Theme Toggle**: Instant class switching (.dark)
- **Button Hovers**: Scale transforms (110%) with rotation effects
- **Gradient Animations**: Canvas-based, 60fps requestAnimationFrame

### Responsive Design
- **Breakpoints**: 
  - Mobile: < 768px (md)
  - Tablet: 768px - 1024px
  - Desktop: > 1024px
  - Max Container: 1800px

### Performance Features
- **Image Optimization**: figma:asset imports for project images
- **Lazy Loading**: ImageWithFallback component for external images
- **Theme Persistence**: Local storage via useState hooks
- **Smooth Navigation**: Anchor link scroll behavior

### Accessibility Features
- **Color Contrast**: WCAG AA compliant color combinations
- **Focus States**: Visible on all interactive elements
- **Semantic HTML**: Proper section and heading hierarchy
- **Alt Text**: Provided for all images
- **Screen Reader**: Compatible button and link labels

This specification provides exact implementation details for recreating every aspect of the Arshaan Khan portfolio website with precise measurements, colors, animations, and functionality.