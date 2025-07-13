# AI Theme & Color Palette Generator

A powerful web-based tool that generates complete, structured theme JSON objects from images, brand colors, or existing websites. Perfect for creating consistent design systems and visual themes for applications, websites, and digital platforms.

## 🎨 Features

### Core Functionality
- **Image-Based Theme Generation**: Upload an image and extract dominant colors to create cohesive themes
- **Color Palette Generation**: Generate themes from custom primary and secondary color selections
- **Website Color Extraction**: Extract color schemes from existing websites (simulation mode)
- **AI-Powered Theme Suggestions**: Intelligent theme generation with multiple variations
- **Real-Time Preview**: Visual preview of generated themes in a simulated interface
- **JSON Export**: Export themes as structured JSON objects for easy integration

### Theme Types Generated
- **Cyber Noir**: Dark, modern themes with vibrant accents
- **Daylight Corporate**: Professional light themes
- **Dynamic Gradient**: Gradient-based themes with dynamic backgrounds
- **Minimalist Focus**: Clean, minimal design themes
- **Modern Glass**: Glassmorphism-inspired themes
- **Neon Pulse**: High-contrast, vibrant themes
- **Executive Suite**: Professional business themes
- **Boardroom**: Corporate dark themes
- **Creative Studio**: Artistic and creative themes
- **Artistic Flow**: Flowing, organic themes
- **Zen Minimal**: Minimalist zen-inspired themes
- **Dark Minimal**: Clean dark minimalist themes

### Image-Specific Themes
When processing images, additional specialized themes are generated:
- **Image Focus - Vibrant**: Uses the most vibrant colors from the image
- **Image Focus - Subtle**: Subtle overlay with image background
- **Image Focus - Gradient Overlay**: Gradient overlays on image backgrounds
- **Image Focus - Blur**: Blurred image backgrounds with enhanced effects

## 🚀 Quick Start

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- No additional software installation required

### Usage

1. **Open the Application**
   ```bash
   # Simply open the index.html file in your browser
   open theme_generator/index.html
   ```

2. **Choose Your Input Method**
   - **From Image**: Upload an inspiration image
   - **From Colors**: Select custom primary and secondary colors
   - **From Website**: Enter a website URL (simulation mode)

3. **Generate Themes**
   - Click the generate button for your chosen method
   - Wait for the AI to process and generate theme variations

4. **Preview and Export**
   - Switch between "Preview" and "JSON" views
   - Copy the JSON output for use in your projects

## 📋 Theme Structure

Each generated theme includes the following properties:

```json
{
  "name": "Theme Name",
  "theme_type": "dark|light",
  "theme_primary_color": "#HEXCODE",
  "theme_secondary_color": "#HEXCODE",
  "primary_text_color": "#HEXCODE",
  "secondary_text_color": "#HEXCODE",
  "stage_background": "gradient|url|color",
  "stage_text_color": "#HEXCODE",
  "event_background": "background_value",
  "screen_saver_background": "#HEXCODE",
  "screen_saver_text_color": "#HEXCODE",
  "name_card_background": "var(--theme-secondary-color)",
  "name_card_text_color": "var(--secondary-text-color)",
  "lower_third_background": "var(--theme-secondary-color)",
  "lower_third_text_color": "var(--secondary-text-color)",
  "sidebar_blur": "200px",
  "sidebar_alpha": 0.05,
  "page_item_alpha": 0.035,
  "ctrl_bar_shade_alpha": 0.5,
  "p2p_panel_shade_alpha": 0.5,
  "name_card_radius": "20px",
  "primary_background_shade": "255, 255, 255",
  "alt_primary_background_shade": "0, 0, 0",
  "logos": [],
  "font_type": "Default",
  "auth_theme": true
}
```

## 🎯 Use Cases

### For Developers
- Generate consistent color schemes for applications
- Create theme variations for different user preferences
- Export structured JSON for theme systems
- Rapid prototyping of visual designs

### For Designers
- Extract color palettes from inspiration images
- Create cohesive design systems
- Generate multiple theme variations quickly
- Visualize themes in a realistic interface preview

### For Product Teams
- Maintain brand consistency across platforms
- Create accessible color combinations
- Generate themes for different contexts (dark/light modes)
- Export themes for development implementation

## 🔧 Technical Details

### Color Processing
- **K-Means Clustering**: Extracts dominant colors from images
- **Luminance Calculation**: Ensures proper contrast ratios
- **Color Harmony**: Generates complementary color combinations
- **Accessibility**: Maintains WCAG contrast guidelines

### Theme Generation Algorithm
1. **Color Analysis**: Extract and sort colors by luminance
2. **Contrast Optimization**: Ensure readable text colors
3. **Background Generation**: Create appropriate background styles
4. **Theme Variation**: Generate multiple theme types
5. **Validation**: Verify color combinations meet accessibility standards

### Browser Compatibility
- Chrome 80+
- Firefox 75+
- Safari 13+
- Edge 80+

## 📁 Project Structure

```
theme_generator/
├── index.html          # Main application file
├── README.md          # This documentation
└── assets/            # Additional assets (if any)
```

## 🎨 Customization

### Adding New Theme Types
To add new theme types, modify the `generateThemesFromPalette` function in the JavaScript code:

```javascript
// Add new theme type
themes.push(createTheme(
    "Your Theme Name",
    "dark|light",
    primaryColor,
    secondaryColor,
    textColor,
    backgroundStyle
));
```

### Modifying Color Processing
Adjust the color extraction algorithm in the `getDominantColors` function:

```javascript
function getDominantColors(pixelData, k) {
    // Modify clustering parameters
    // Adjust color sampling frequency
    // Change color space processing
}
```

## 🔍 Troubleshooting

### Common Issues

**Image Upload Not Working**
- Ensure the image file is a valid image format (JPG, PNG, GIF)
- Check browser console for JavaScript errors
- Verify file size is reasonable (< 10MB)

**Theme Generation Fails**
- Try uploading a different image with more distinct colors
- Ensure the image has sufficient color variety
- Check that the image loads completely before processing

**Preview Not Displaying**
- Refresh the page and try again
- Check browser console for errors
- Ensure JavaScript is enabled

### Performance Tips
- Use images with clear, distinct colors for better results
- Avoid very large images (resize to < 1000px width/height)
- Close other browser tabs to free up memory

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly with different image types
5. Submit a pull request

### Development Guidelines
- Maintain accessibility standards
- Test with various image types and sizes
- Ensure cross-browser compatibility
- Add comments for complex color processing logic

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- Built with [Tailwind CSS](https://tailwindcss.com/) for styling
- Uses [Inter font](https://fonts.google.com/specimen/Inter) for typography
- Color processing algorithms based on established color theory principles
- Preview interface inspired by modern video conferencing platforms

## 📞 Support

For questions, issues, or feature requests:
1. Check the troubleshooting section above
2. Review browser console for error messages
3. Open an issue in the repository
4. Contact the development team

---

**Note**: This tool generates themes based on color analysis and design principles. Always review generated themes for your specific use case and ensure they meet your brand guidelines and accessibility requirements. 