# Gallery Media Setup Instructions

## Adding Your Own Gallery Media

1. **Add Images and Videos to the `images/` folder:**
   - Place your gallery media in the `/images/` directory
   - **Image formats:** .jpg, .jpeg, .png, .gif, .webp (JPG recommended for best compatibility)
   - **Video formats:** .mp4, .mov, .webm, .avi, .mkv
   - Recommended image size: 800x600 pixels or larger for best quality
   - Videos will automatically show with play button overlay

2. **Update the `images/index.json` file (Optional):**
   - Add entries for each new media file
   - Follow this format:
   ```json
   {
     "src": "images/your-media-file.jpg",
     "alt": "Descriptive text for the media",
     "caption": "Caption that appears below the media"
   }
   ```

3. **Example JSON structure:**
   ```json
   [
     {
       "src": "images/youth-fellowship.jpg",
       "alt": "Youth Fellowship Meeting",
       "caption": "Our weekly youth fellowship gathering"
     },
     {
       "src": "images/worship-video.mp4", 
       "alt": "Praise and Worship Session",
       "caption": "Sunday morning worship highlights"
     },
     {
       "src": "images/phone-photo.heic",
       "alt": "iPhone Photo",
       "caption": "Direct from iPhone camera"
     }
   ]
   ```

## Current Setup

The gallery is now configured to:
- **Auto-detect images and videos** from common file names
- **Support HEIC images** from iPhones directly
- **Support video files** with play button overlay and modal playback
- Display placeholder message if no media files are found
- Show error placeholders for individual missing files
- Support modal viewing with click-to-enlarge for images and full-screen video playback
- Be fully responsive for mobile and desktop

## Supported File Naming Patterns

The system automatically looks for files named:
- **Images:** gallery1.jpg, photo1.png, image1.jpg, youth1.jpg, 1.jpg, etc.
- **iPhone Photos:** IMG_1362.jpg, IMG_1961.jpg (after conversion), etc.
- **Videos:** video1.mp4, gallery1.mov, 1.mp4, etc.
- **Your existing:** Church_BG.JPG (found in images folder)

## Important Notes

**Recommended Image Format:** JPG/JPEG for best browser compatibility
- All browsers support JPG images perfectly
- Smaller file sizes for web use
- No compatibility issues

**Converting HEIC to JPG:**
1. **iPhone Photos App**: Select image → Share → Save to Files → Choose JPEG
2. **Mac Preview**: Open HEIC → File → Export → JPEG format
3. **Online Converters**: heictojpg.com, convertio.co
4. **iPhone Settings**: Camera → Formats → "Most Compatible" (future photos as JPG)

**Your Current Setup:**
- ✅ `Church_BG.JPG` - Ready to go
- 🔄 `IMG_1362.HEIC` → Convert to `IMG_1362.jpg`
- 🔄 `IMG_1961.HEIC` → Convert to `IMG_1961.jpg`

## Testing

After converting your HEIC files to JPG:
1. Replace the HEIC files in `images/` folder with JPG versions
2. Update the JSON file with new .jpg extensions
3. Refresh the website to see all images

**Steps to Complete:**
1. Convert `IMG_1362.HEIC` → `IMG_1362.jpg`
2. Convert `IMG_1961.HEIC` → `IMG_1961.jpg`
3. Upload the new JPG files to replace HEIC files
4. Update `images/index.json` to change `.HEIC` to `.jpg`

**Special Features:**
- **Universal Compatibility:** JPG works in all browsers
- **Video Support:** MP4/MOV files with play button overlay
- **Modal Viewing:** Click to enlarge images or play videos full-screen
- **Auto-Detection:** No JSON editing required for standard file names
- **Responsive Design:** Works perfectly on mobile and desktop

The current JSON file contains sample entries that you can update with your converted JPG files.
