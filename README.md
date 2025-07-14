# Tonmoy Md Towfiq Zia - Portfolio Website

A modern, responsive portfolio website for Tonmoy Md Towfiq Zia, a Frontend Developer based in Shimane, Japan. This portfolio showcases professional skills, projects, and cultural awareness with bilingual support (English/Japanese).

## 🌟 Features

- **Responsive Design**: Optimized for all devices and screen sizes
- **Bilingual Support**: Toggle between English and Japanese
- **Dark/Light Mode**: User preference with system detection
- **Smooth Animations**: Powered by Framer Motion
- **Modern UI/UX**: Clean, minimalist design with professional aesthetics
- **Contact Form**: Functional contact form with EmailJS integration
- **SEO Optimized**: Proper meta tags and semantic HTML
- **Performance Optimized**: Fast loading and smooth interactions

## 🛠️ Technologies Used

- **Frontend Framework**: React.js 18
- **Styling**: Tailwind CSS
- **Animations**: Framer Motion
- **Icons**: Lucide React
- **Contact Form**: EmailJS
- **Build Tool**: Create React App
- **Deployment**: Ready for Vercel/Netlify

## 📁 Project Structure

```
src/
├── components/
│   ├── Header.js          # Navigation with theme/language toggles
│   ├── Hero.js            # Hero section with introduction
│   ├── About.js           # About section with background
│   ├── Skills.js          # Skills and technologies
│   ├── Projects.js        # Featured projects showcase
│   ├── Contact.js         # Contact form and information
│   └── Footer.js          # Footer with social links
├── contexts/
│   ├── LanguageContext.js # Bilingual support context
│   └── ThemeContext.js    # Dark/light mode context
├── App.js                 # Main application component
├── index.js              # Application entry point
└── index.css             # Global styles and Tailwind imports
```

## 🚀 Getting Started

### Prerequisites

- Node.js (version 14 or higher)
- npm or yarn package manager

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd tonmoy-portfolio
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start the development server**
   ```bash
   npm start
   ```

4. **Open your browser**
   Navigate to `http://localhost:3000` to view the portfolio

### Build for Production

```bash
npm run build
```

This creates an optimized production build in the `build` folder.

## 📧 Contact Form Setup

To enable the contact form functionality:

1. **Sign up for EmailJS**
   - Visit [EmailJS](https://www.emailjs.com/)
   - Create a free account

2. **Configure EmailJS**
   - Create an email service
   - Create an email template
   - Get your service ID, template ID, and public key

3. **Update Contact.js**
   ```javascript
   const serviceId = 'your_service_id';
   const templateId = 'your_template_id';
   const publicKey = 'your_public_key';
   ```

4. **Uncomment the EmailJS send function**
   ```javascript
   await emailjs.send(serviceId, templateId, templateParams, publicKey);
   ```

## 🎨 Customization

### Colors
Update the color scheme in `tailwind.config.js`:

```javascript
colors: {
  primary: {
    // Your custom color palette
  }
}
```

### Content
Update personal information in:
- `src/contexts/LanguageContext.js` - All text content
- `src/components/Projects.js` - Project information
- `src/components/Skills.js` - Skills and technologies
- `src/components/About.js` - Personal background

### Fonts
The project uses Inter and Noto Sans JP fonts. Update in `public/index.html` and `tailwind.config.js` if needed.

## 🌐 Deployment

### Vercel (Recommended)

1. **Connect your repository to Vercel**
2. **Configure build settings**:
   - Build Command: `npm run build`
   - Output Directory: `build`
3. **Deploy**

### Netlify

1. **Connect your repository to Netlify**
2. **Configure build settings**:
   - Build Command: `npm run build`
   - Publish Directory: `build`
3. **Deploy**

## 📱 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers

## 🔧 Development

### Available Scripts

- `npm start` - Start development server
- `npm run build` - Build for production
- `npm test` - Run tests
- `npm run eject` - Eject from Create React App

### Code Style

- Use functional components with hooks
- Follow React best practices
- Use Tailwind CSS for styling
- Implement responsive design
- Add proper accessibility attributes

## 🎯 Target Audience

- Japanese IT companies and recruiters
- HR teams evaluating international frontend developers
- Employers seeking bilingual, adaptable web engineers

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Tonmoy Md Towfiq Zia**
- Frontend Developer
- Based in Shimane, Japan
- Email: tonmoy.zia@example.com
- GitHub: [@tonmoy](https://github.com/tonmoy)
- LinkedIn: [Tonmoy Md Towfiq Zia](https://linkedin.com/in/tonmoy)

## 🙏 Acknowledgments

- Design inspiration from modern portfolio websites
- Japanese cultural elements and design principles
- Open source community for amazing tools and libraries

---

**Made with ❤️ in Japan**