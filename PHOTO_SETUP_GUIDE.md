# 📷 Photo Setup Guide for Portfolio Website

This guide explains how to add your profile photo to the Hero section of your portfolio website.

## 🎯 Current Setup

The Hero component now includes **3 different photo options** that you can choose from:

### Option 1: Real Profile Photo (Recommended)
```jsx
<img 
  src="/profile-photo.jpg" 
  alt="Tonmoy Md Towfiq Zia"
  className="w-full h-full object-cover rounded-full"
  onError={(e) => {
    e.target.style.display = 'none';
    e.target.nextSibling.style.display = 'flex';
  }}
/>
```

### Option 2: Avatar with Initials (Current Default)
```jsx
<div className="w-full h-full rounded-full bg-gradient-to-br from-primary-100 to-primary-200 dark:from-primary-800 dark:to-primary-900 flex items-center justify-center">
  <span className="text-4xl font-bold text-primary-600 dark:text-primary-400">
    T
  </span>
</div>
```

### Option 3: Professional Avatar Icon
```jsx
<div className="w-full h-full rounded-full bg-gradient-to-br from-blue-100 to-blue-200 dark:from-blue-800 dark:to-blue-900 flex items-center justify-center">
  <svg className="w-16 h-16 text-blue-600 dark:text-blue-400" fill="currentColor" viewBox="0 0 24 24">
    <path d="M12 12c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm0 2c-2.67 0-8 1.34-8 4v2h16v-2c0-2.66-5.33-4-8-4z"/>
  </svg>
</div>
```

## 🚀 How to Add Your Photo

### Method 1: Static Photo (Recommended)

1. **Prepare your photo:**
   - Use a high-quality, professional headshot
   - Recommended size: 400x400px or larger (square format)
   - Supported formats: JPG, PNG, WebP
   - File size: Keep under 500KB for optimal loading

2. **Add photo to public folder:**
   ```
   public/
   ├── index.html
   └── profile-photo.jpg  ← Add your photo here
   ```

3. **Update Hero.js:**
   - Open `src/components/Hero.js`
   - Find the "Option 1: Real Photo" section
   - Remove the `{/* */}` comment markers around the img tag
   - Comment out "Option 2: Avatar with Initials" by adding `{/* */}` around it

   **Before:**
   ```jsx
   {/* <img 
     src="/profile-photo.jpg" 
     alt="Tonmoy Md Towfiq Zia"
     className="w-full h-full object-cover rounded-full"
   /> */}
   
   <div className="w-full h-full rounded-full bg-gradient-to-br from-primary-100 to-primary-200">
     <span className="text-4xl font-bold text-primary-600 dark:text-primary-400">
       T
     </span>
   </div>
   ```

   **After:**
   ```jsx
   <img 
     src="/profile-photo.jpg" 
     alt="Tonmoy Md Towfiq Zia"
     className="w-full h-full object-cover rounded-full"
     onError={(e) => {
       e.target.style.display = 'none';
       e.target.nextSibling.style.display = 'flex';
     }}
   />
   
   {/* <div className="w-full h-full rounded-full bg-gradient-to-br from-primary-100 to-primary-200">
     <span className="text-4xl font-bold text-primary-600 dark:text-primary-400">
       T
     </span>
   </div> */}
   ```

### Method 2: Dynamic Photo Upload (Advanced)

1. **Enable upload functionality:**
   - Open `src/components/Hero.js`
   - Find the "Photo Upload Option" section
   - Remove the `{/* */}` comment markers around the upload section

2. **Features included:**
   - File input for selecting photos
   - Real-time preview
   - Automatic fallback to initials if photo fails
   - Client-side only (photo not saved permanently)

## 🎨 Photo Styling Features

- **Circular crop:** Photos are automatically cropped to circular shape
- **Gradient border:** Beautiful gradient border around the photo
- **Shadow effect:** Elegant shadow for depth
- **Responsive:** Scales properly on all devices
- **Dark mode support:** Adapts to light/dark themes
- **Error handling:** Falls back to initials if photo fails to load

## 📱 Best Practices

### Photo Requirements:
- **Format:** JPG or PNG
- **Size:** 400x400px minimum (square aspect ratio)
- **Quality:** High resolution, professional appearance
- **Background:** Clean, preferably solid color or blurred
- **Lighting:** Well-lit, clear facial features
- **Expression:** Professional, friendly smile

### File Naming:
- Use descriptive names: `profile-photo.jpg`
- Avoid spaces: Use hyphens or underscores
- Keep it simple and memorable

### Performance Tips:
- Optimize image size (use tools like TinyPNG)
- Consider WebP format for better compression
- Test loading speed on different devices

## 🔧 Troubleshooting

### Photo not showing?
1. Check file path: Ensure photo is in `/public/` folder
2. Verify file name matches the src attribute
3. Check browser console for errors
4. Ensure photo file is not corrupted

### Photo looks distorted?
1. Use square aspect ratio (1:1)
2. Check if `object-cover` class is applied
3. Verify image resolution is adequate

### Upload feature not working?
1. Ensure upload section is uncommented
2. Check browser compatibility (modern browsers only)
3. Verify file size is reasonable (<5MB)

## 🌟 Additional Customization

### Change photo size:
```jsx
// Current: w-32 h-32 (128px)
<div className="w-40 h-40 mx-auto rounded-full"> // 160px
<div className="w-36 h-36 mx-auto rounded-full"> // 144px
<div className="w-28 h-28 mx-auto rounded-full"> // 112px
```

### Modify border gradient:
```jsx
// Current gradient
bg-gradient-to-r from-primary-400 to-primary-600

// Alternative gradients
bg-gradient-to-r from-blue-400 to-purple-600
bg-gradient-to-r from-green-400 to-blue-500
bg-gradient-to-r from-pink-400 to-red-600
```

### Add hover effects:
```jsx
<motion.div
  whileHover={{ scale: 1.1, rotate: 5 }}
  transition={{ duration: 0.3 }}
>
  {/* Photo content */}
</motion.div>
```

## 📞 Support

If you need help implementing any of these photo options:
1. Check the browser console for error messages
2. Verify all file paths are correct
3. Test with different photo files
4. Ensure React development server is running

---

**Note:** The website currently defaults to showing initials ("T") as a professional placeholder. Simply follow Method 1 above to replace it with your actual photo!