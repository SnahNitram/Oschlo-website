# Oschlo.co Website Redesign - Product Requirements Document

## Project Overview

**Project Name:** Oschlo.co Website Redesign  
**Version:** 1.0  
**Date:** July 2025  
**Owner:** Oschlo Team  

### Executive Summary
Complete redesign of Oschlo.co to create a lightweight, AI-optimized website with Notion as CMS, emphasizing clean typography, mobile optimization, and seamless content management for blog and landing pages.

## Business Objectives

### Primary Goals
1. **Reduce Content Management Friction** - Enable team to publish content quickly via Notion
2. **Improve Performance** - Achieve sub-2 second load times on mobile
3. **Enhance User Experience** - Clean, professional design reflecting AI expertise
4. **Increase Conversion** - Optimize landing pages for service inquiries
5. **Maintain SEO Value** - Preserve existing URL structure and search rankings
6. **Consolidate Content** - Bring all blog content under main domain management

### Success Metrics
- Page load time: <2 seconds (mobile)
- Content publishing time: <5 minutes from Notion to live
- Contact form conversion rate: +25% improvement
- Blog engagement: +40% time on page
- Core Web Vitals: All green scores

## Target Audience

### Primary Users
1. **Norwegian Enterprise Decision Makers** - CTOs, Product Leaders, Innovation Managers
2. **Product Management Community** - Product managers seeking training and insights
3. **AI Implementation Teams** - Technical teams evaluating AI consultancy

### User Journeys
1. **Service Discovery:** Homepage → Service pages → Contact form
2. **Content Consumption:** Blog discovery → Article reading → Newsletter signup
3. **Course Interest:** Homepage/Blog → Course page → Registration

## Technical Requirements

### Architecture & Performance
- **Framework:** Modern static site generator (Next.js, Nuxt, or similar)
- **Hosting:** Edge-optimized hosting (Vercel, Netlify, or Cloudflare Pages)
- **Performance Target:** 
  - First Contentful Paint: <1.5s
  - Largest Contentful Paint: <2.5s
  - Cumulative Layout Shift: <0.1
- **Mobile-First:** Responsive design with mobile optimization priority

### CMS Integration (Notion)
- **Content Source:** Notion database as primary CMS
- **API Integration:** Notion API for content fetching
- **Content Types:**
  - Blog posts (title, content, tags, publish date, featured image)
  - Service pages (structured content blocks)
  - Team member profiles
  - Course information
- **Publishing Workflow:** 
  - Write in Notion → Mark as "Published" → Auto-deploy to site
  - Preview mode for draft content
  - Scheduled publishing capability

### URL Structure Preservation
```
/                                    (Homepage)
/kontakt-oss                        (Contact - Norwegian)
/contact                            (Contact - English alternative)
/tjenester/                         (Services section)
/tjenester/ai-readiness             (Existing service page)
/tjenester/[service-slug]           (Additional services)
/kurs/                              (Courses section)
/kurs/product-discovery             (Existing course)
/kurs/[course-slug]                 (Additional courses)
/blogg/                             (Blog listing)
/blogg/[post-slug]                  (Individual posts)
/om-oss                             (About us)
/karriere                           (Careers)
```

## Design Requirements

### Visual Design System

#### Typography
- **Primary Font:** Typewriter-style font (JetBrains Mono, Source Code Pro, or similar)
- **Secondary Font:** Clean sans-serif for body text (Inter, System fonts)
- **Hierarchy:**
  - H1: 2.5rem, typewriter font, bold
  - H2: 2rem, typewriter font, medium
  - H3: 1.5rem, typewriter font, medium
  - Body: 1rem, sans-serif, regular
  - Code/highlight: 0.875rem, typewriter font

#### Color Palette
- **Light Mode:**
  - Background: #FFFFFF
  - Text Primary: #1a1a1a
  - Text Secondary: #666666
  - Accent: #0066CC (Oschlo blue)
  - Border: #E5E5E5
  - Code background: #F8F9FA
- **Dark Mode:**
  - Background: #0a0a0a
  - Text Primary: #FFFFFF
  - Text Secondary: #A0A0A0
  - Accent: #4A9EFF
  - Border: #2a2a2a
  - Code background: #1a1a1a

#### Layout Principles
- **Grid:** 12-column responsive grid
- **Spacing:** 8px base unit, multiples for larger spaces
- **Container:** Max-width 1200px, centered
- **Whitespace:** Generous use for clarity and readability

### Component Library

#### Header (Fixed)
- Logo (Oschlo wordmark)
- Navigation menu (Services, Blog, About, Contact)
- Dark mode toggle
- Language switcher (NO/EN)
- Mobile hamburger menu

#### Footer (Fixed)
- Company information
- Quick links
- Social media icons
- Newsletter signup
- Copyright notice

#### Content Components
- **Hero Section:** Large headline, subtext, CTA button
- **Service Cards:** Icon, title, description, link
- **Blog Card:** Featured image, title, excerpt, date, tags
- **Team Member Card:** Photo, name, role, bio
- **Contact Form:** Name, email, company, message, submit
- **Newsletter Signup:** Email input, subscribe button

### Responsive Behavior
- **Desktop (1200px+):** Full layout with sidebar options
- **Tablet (768px-1199px):** Adjusted spacing, stacked elements
- **Mobile (320px-767px):** Single column, touch-optimized

## Functional Requirements

### Core Features

#### Content Management
- **Notion Integration:** Real-time sync with Notion databases
- **Content Preview:** Ability to preview drafts before publishing
- **Media Management:** Image optimization and CDN delivery
- **SEO Fields:** Meta titles, descriptions, social media images

#### User Interface
- **Navigation:** Sticky header with smooth scrolling
- **Search:** Blog search functionality
- **Filtering:** Tag-based blog filtering
- **Dark Mode:** System preference detection + manual toggle
- **Language Toggle:** Norwegian/English content switching

#### Performance Features
- **Image Optimization:** Next-gen formats (WebP, AVIF)
- **Lazy Loading:** Images and components below fold
- **Code Splitting:** Route-based JavaScript bundles
- **Caching:** Aggressive caching for static content

### Blog Features
- **Article Pages:** Full article display with typography optimization
- **Related Posts:** Algorithm-based suggestions
- **Social Sharing:** LinkedIn, Twitter, email sharing
- **Reading Time:** Estimated reading time display
- **Table of Contents:** Auto-generated for long articles
- **Comments:** Integration with comment system (optional)

### Service Pages
- **Structured Content:** Flexible content blocks from Notion
- **Lead Generation:** Contact forms with service-specific fields
- **Case Studies:** Client work showcases
- **Testimonials:** Client feedback display

## Technical Specifications

### Development Stack
- **Frontend Framework:** Next.js 14+ or Nuxt 3+
- **Styling:** Tailwind CSS for utility-first styling
- **Typography:** Custom web fonts with fallbacks
- **Icons:** Lucide icons or similar minimal icon set
- **Forms:** React Hook Form or similar validation
- **Analytics:** Google Analytics 4 or privacy-focused alternative

### Content Pipeline
- **Source:** Notion databases
- **Build:** Static generation with incremental regeneration
- **Deploy:** Automated deployment on content changes
- **CDN:** Global content delivery network

### SEO Implementation
- **Meta Tags:** Dynamic generation from Notion content
- **Structured Data:** JSON-LD for articles and organization
- **Sitemap:** Auto-generated XML sitemap
- **Robots.txt:** Search engine guidance
- **Redirects:** 301 redirects for URL changes

### Accessibility
- **WCAG 2.1 AA Compliance**
- **Keyboard Navigation:** Full site navigable via keyboard
- **Screen Reader Support:** Proper ARIA labels and semantic HTML
- **Color Contrast:** Minimum 4.5:1 ratio for text
- **Focus Indicators:** Clear visual focus states

## Content Strategy

### Content Types
1. **Homepage:** Company overview, services highlight, recent blog posts
2. **Service Pages:** Detailed service descriptions, case studies, contact forms
3. **Blog Posts:** Thought leadership, tutorials, industry insights
4. **About Page:** Team, company story, values
5. **Course Pages:** Training descriptions, curricula, registration

### Content Migration
- **Priority 1:** Homepage, main service pages, contact
- **Priority 2:** Existing blog posts from oschlo.co/blogg/
- **Priority 3:** Additional pages (about, careers, courses)
- **Note:** Medium blog content is discontinued and will not be migrated

## User Experience Requirements

### Navigation Experience
- **Clear Information Architecture:** Logical grouping and hierarchy
- **Breadcrumbs:** Clear path indication on deep pages
- **Search Functionality:** Site-wide search with auto-complete
- **Related Content:** Contextual suggestions throughout site

### Loading Experience
- **Progressive Loading:** Critical content first, enhanced progressively
- **Loading States:** Clear feedback during content loading
- **Error Handling:** Graceful degradation and error messages
- **Offline Support:** Basic offline browsing for cached content

### Conversion Optimization
- **Contact Forms:** Multiple touchpoints with varied complexity
- **Call-to-Action Buttons:** Clear, prominent, action-oriented
- **Social Proof:** Client logos, testimonials, case studies
- **Trust Signals:** Team photos, certifications, contact information

## Launch Requirements

### Pre-Launch
- **Content Audit:** Review and optimize all migrated content
- **Performance Testing:** Core Web Vitals validation
- **Accessibility Audit:** WCAG compliance verification
- **Cross-Browser Testing:** Chrome, Firefox, Safari, Edge
- **Mobile Testing:** iOS Safari, Android Chrome
- **SEO Setup:** Analytics, Search Console, redirects

### Launch Process
1. **Soft Launch:** Deploy to staging with limited audience
2. **Redirect Setup:** Implement 301 redirects for changed URLs
3. **DNS Migration:** Point domain to new hosting
4. **Monitor:** Track performance, errors, and user feedback
5. **Optimize:** Address any issues discovered post-launch

### Post-Launch
- **Performance Monitoring:** Ongoing Core Web Vitals tracking
- **Content Publishing:** Train team on Notion workflow
- **SEO Monitoring:** Track rankings and fix any drops
- **User Feedback:** Collect and implement user suggestions

## Success Criteria

### Technical Metrics
- Page Speed: 95+ Lighthouse score
- Accessibility: 100 Lighthouse accessibility score
- SEO: No significant ranking drops
- Uptime: 99.9% availability

### Business Metrics
- Contact form submissions: +25% increase
- Blog engagement: +40% time on page
- Email signups: +30% increase
- Mobile traffic: Improved user experience metrics

### Content Metrics
- Publishing frequency: Daily capability
- Content updates: Real-time sync with Notion
- Team adoption: 100% team using Notion workflow
- Content quality: Consistent formatting and presentation

## Risk Mitigation

### Technical Risks
- **API Limitations:** Notion API rate limits → Implement caching and incremental builds
- **Performance Issues:** Heavy images → Automated optimization pipeline
- **Browser Compatibility:** Modern features → Progressive enhancement strategy

### Content Risks
- **Content Loss:** Migration errors → Comprehensive backup strategy
- **SEO Impact:** URL changes → Detailed redirect mapping
- **User Confusion:** New design → Gradual rollout with user feedback

### Business Risks
- **Downtime:** Migration issues → Blue-green deployment strategy
- **Team Adoption:** Workflow changes → Training and documentation
- **Cost Overruns:** Scope creep → Fixed scope with clear change process

## Appendices

### Browser Support Matrix
- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+
- Mobile Safari iOS 14+
- Chrome Mobile Android 90+

### Third-Party Integrations
- Notion API (content management)
- Google Analytics (analytics)
- EmailOctopus or ConvertKit (newsletter)
- Calendly (meeting booking)
- LinkedIn (social integration)

### Performance Budget
- JavaScript bundle: <200KB gzipped
- CSS bundle: <50KB gzipped
- Images: WebP/AVIF with fallbacks
- Fonts: 2 font families maximum
- Third-party scripts: Minimal, async loaded