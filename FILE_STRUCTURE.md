# Augustine University Website - File Structure

## Directory Organization

```
AUI-web-clone/
├── index.html                                    # Root homepage
├── FILE_STRUCTURE.md                             # This file
├── Augustine University Website/
│   ├── index.html                               # Alternative homepage entry
│   ├── Home/
│   │   ├── index.html                          # Home page
│   │   ├── style_hom.css                       # Home page styles
│   │   └── Augustine.university.logo.png       # University logo
│   ├── About/
│   │   ├── index.html                          # About page
│   │   ├── About.html                          # Alternative About page file
│   │   ├── style_abt.css                       # About page styles
│   │   ├── Augustine.university.logo.png       # University logo
│   │   ├── DEAN.jpg                            # Dean portrait image
│   │   └── SUB-DEAN.jpg                        # Sub-Dean portrait image
│   ├── Department/
│   │   ├── Department.html                     # Department page
│   │   ├── style_dep.css                       # Department page styles
│   │   ├── IMG-20260519-WA0024.jpg             # HOD portrait
│   │   ├── JohnBosco.jpg                       # Staff portraits
│   │   ├── Rufai.jpg
│   │   ├── Akinmerese.jpg
│   │   ├── Ibitola.jpg
│   │   ├── Akinyemi.jpg
│   │   ├── Omisore.jpg
│   │   ├── Agagu.jpg
│   │   ├── Ogunbawo.jpg
│   │   ├── Egume.jpg
│   │   ├── Ayo.jpg
│   │   ├── Abel.jpg
│   │   ├── Gbenga.jpg
│   │   ├── Adediran.jpg
│   │   ├── Alao.jpg
│   │   └── Akinola.jpg
│   ├── Home/
│   │   ├── Augustine.university.logo.png
│   │   ├── Computer-Science-Page-Header-2048x1197.jpg
│   │   ├── information-technology.jpg
│   │   ├── what-is-cybersecurity.jpg
│   │   ├── what-is-data-science.jpg
│   │   ├── Sen.jpg
│   │   ├── AUI.jpg
│   │   └── WhatsApp Image 2024-08-29 at 4.48.19 PM.jpeg
└── portal.html                                   # Student portal page (referenced but not provided)
```

## File Linking Guidelines

### Strict Path Conventions

#### From Root (`/index.html`)
- Home: `Augustine University Website/Home/index.html`
- About: `Augustine University Website/About/index.html`
- Department: `Augustine University Website/Department/Department.html`
- Portal: `portal.html`

#### From Home Page (`Augustine University Website/Home/index.html`)
- Root: `../../index.html`
- About: `../About/index.html`
- Department: `../Department/Department.html`
- Portal: `../../portal.html`

#### From About Page (`Augustine University Website/About/index.html`)
- Root: `../../index.html`
- Home: `../Home/index.html`
- Department: `../Department/Department.html`
- Portal: `../../portal.html`

#### From Department Page (`Augustine University Website/Department/Department.html`)
- Root: `../../index.html`
- Home: `../Home/index.html`
- About: `../About/index.html`
- Portal: `../../portal.html`

### Image Path Conventions

#### Images in Department folder
- Reference images from Home: `../Home/image-name.jpg`
- Local staff images: `./staff-image.jpg` or `staff-image.jpg`

#### Images in About folder
- Reference images from Home: `../Home/image-name.jpg`
- Local portrait images: `./DEAN.jpg` or `DEAN.jpg`

#### Images in Home folder
- Local images: `./image-name.jpg` or `image-name.jpg`

#### Images from root
- Home images: `Augustine University Website/Home/image-name.jpg`
- Logos: `Augustine University Website/Home/Augustine.university.logo.png`

## CSS and JavaScript Linking

### From Index pages in subdirectories
```html
<!-- From Augustine University Website/About/index.html -->
<link rel="stylesheet" href="/About/style_abt.css" />

<!-- From Augustine University Website/Department/Department.html -->
<link rel="stylesheet" href="/Department/style_dep.css"/>

<!-- From Augustine University Website/Home/index.html -->
<link rel="stylesheet" href="style_hom.css">
```

### From Root index.html
```html
<!-- Assets from subdirectories -->
<link rel="stylesheet" href="Augustine University Website/Home/style_hom.css" />
<img src="Augustine University Website/Home/Augustine.university.logo.png" />
```

## Navigation Menu Links Reference

### Navbar Link Structure (Consistent Across All Pages)
```html
<ul class="navbar-links">
  <li><a href="[HOME_LINK]">Home</a></li>
  <li><a href="[ABOUT_LINK]">About</a></li>
  <li class="dropdown-parent">
    <a href="[DEPARTMENT_LINK]">Department</a>
    <div class="dropdown-menu">
      <a href="[DEPARTMENT_LINK]#staff">Staff</a>
      <a href="[DEPARTMENT_LINK]#courses">Courses</a>
    </div>
  </li>
  <li class="dropdown-parent">
    <a href="[PORTAL_LINK]">Student Portal</a>
    <div class="dropdown-menu">
      <a href="[PORTAL_LINK]#course-registration">Course Registration</a>
      <a href="[PORTAL_LINK]#exam-result">Exam Result</a>
      <a href="[PORTAL_LINK]#payment-receipts">Payment Receipts</a>
      <a href="[PORTAL_LINK]#student-profile">Student Profile</a>
    </div>
  </li>
</ul>
```

## Summary

| Page Location | Home Link | About Link | Department Link | Portal Link |
|---|---|---|---|---|
| `/index.html` | `Augustine University Website/Home/index.html` | `Augustine University Website/About/index.html` | `Augustine University Website/Department/Department.html` | `portal.html` |
| `/Augustine University Website/Home/index.html` | `index.html` | `../About/index.html` | `../Department/Department.html` | `../../portal.html` |
| `/Augustine University Website/About/index.html` | `../Home/index.html` | `index.html` | `../Department/Department.html` | `../../portal.html` |
| `/Augustine University Website/Department/Department.html` | `../Home/index.html` | `../About/index.html` | `Department.html` | `../../portal.html` |

