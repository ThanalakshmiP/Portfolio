# Thanalakshmi Paulraj - Portfolio (Vue.js 2)

This is a Vue.js 2 conversion of your HTML/CSS/JS portfolio with the exact same UI, colors, and functionality.

## Project Structure

```
portfolio-vue/
├── public/
│   └── index.html
├── src/
│   ├── components/
│   │   ├── Navigation.vue
│   │   ├── Hero.vue
│   │   ├── Experience.vue
│   │   └── Projects.vue
│   ├── App.vue
│   └── main.js
├── package.json
└── vue.config.js
```

## Components

### 1. Navigation.vue
- Sticky navigation bar with links to sections
- Responsive design

### 2. Hero.vue
- Hero section with typing animation effect
- Displays rotating roles (Frontend Developer, UI/UX Designer, etc.)
- Background gradient changes with each role
- Call-to-action buttons

### 3. Experience.vue
- Timeline-based experience display
- Shows professional experience with company details
- Technologies used displayed as badges
- Hover effects on cards

### 4. Projects.vue
- Project cards with alternating layout (left-right)
- Each project displays:
  - Project image
  - Title and description
  - Technology stack badges
  - Feature list
- Hover effects with shadow and transform

## Setup Instructions

1. **Install Dependencies**
   ```bash
   npm install
   ```

2. **Run Development Server**
   ```bash
   npm run serve
   ```
   The application will be available at `http://localhost:8080`

3. **Build for Production**
   ```bash
   npm run build
   ```
   This will create a `dist/` folder with optimized production files

## Features Preserved

✅ Exact same UI design and layout
✅ Same color scheme (#FDB515 yellow/gold, gradients)
✅ Typing animation effect in hero section
✅ Background gradient changes based on current role
✅ Timeline-based experience section
✅ Alternating project card layouts
✅ All hover effects and transitions
✅ Responsive design for mobile devices
✅ Smooth scrolling navigation

## Key Differences from HTML Version

- **Component-based**: Code is organized into reusable Vue components
- **Data-driven**: Projects and experience are stored in data() and rendered with v-for
- **Reactive**: Typing animation uses Vue's reactivity system
- **Maintainable**: Easy to add/remove projects or experiences by updating data
- **Scoped styles**: Each component has its own scoped CSS

## Customization

### Adding New Projects
Edit `components/Projects.vue` and add objects to the `projects` array:

```javascript
{
  title: 'Project Name',
  image: 'image-url',
  technologies: ['Vue.js', 'Node.js'],
  description: 'Project description',
  features: ['Feature 1', 'Feature 2']
}
```

### Adding Experience
Edit `components/Experience.vue` and add objects to the `experiences` array:

```javascript
{
  company: 'Company Name',
  title: 'Job Title',
  duration: 'Date Range',
  description: 'Job description',
  technologies: ['Tech1', 'Tech2']
}
```

### Modifying Typing Roles
Edit the `roles` array in `components/Hero.vue`:

```javascript
roles: [
  { text: "Your Role", color: "#HexColor" }
]
```

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## License

Personal Portfolio Project
