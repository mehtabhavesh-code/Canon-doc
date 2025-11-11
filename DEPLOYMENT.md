# Deployment Guide for Vercel

This guide will help you deploy the Character Consistency Tracker to Vercel.

## Prerequisites

1. A Vercel account (sign up at [vercel.com](https://vercel.com))
2. Vercel CLI installed (optional, for command-line deployment)
3. Git repository (optional, but recommended)

## Quick Deploy (Recommended)

### Option 1: Deploy via Vercel Dashboard

1. **Prepare your files:**
   - Ensure all files are in the `Canon 2` folder
   - All HTML files should be in the root of this folder

2. **Deploy:**
   - Go to [vercel.com/new](https://vercel.com/new)
   - Import your Git repository (if using Git) OR
   - Drag and drop the `Canon 2` folder directly to Vercel dashboard
   - Vercel will auto-detect it as a static site

3. **Configure (if needed):**
   - Project Name: `canon-character-tracker` (or your preferred name)
   - Framework Preset: Other (or Static Site)
   - Root Directory: `Canon 2` (if deploying from parent directory)

4. **Deploy:**
   - Click "Deploy"
   - Wait for build to complete
   - Your site will be live at `your-project.vercel.app`

### Option 2: Deploy via Vercel CLI

1. **Install Vercel CLI:**
   ```bash
   npm i -g vercel
   ```

2. **Navigate to project:**
   ```bash
   cd "Canon 2"
   ```

3. **Deploy:**
   ```bash
   vercel
   ```

4. **For production:**
   ```bash
   vercel --prod
   ```

## File Structure

Your deployment should include:
```
Canon 2/
├── index.html (main hub)
├── character_dashboard.html
├── character_arc_comparison.html
├── relationship_journey.html
├── story_intensity_timeline.html
├── continuity_issues.html
├── continuity_health_dashboard.html
├── plot_interconnections.html
├── plot_threads_gantt.html
├── timeline_sequence.html
├── power_dynamics.html
├── character_radar_alessandra.html
├── character_radar_edgar.html
├── character_consistency_tracker.md
├── VISUALIZATION_GUIDE.md
├── README.md
├── vercel.json (configuration)
└── package.json (metadata)
```

## Configuration

The `vercel.json` file is already configured with:
- Static site routing
- Proper content-type headers for HTML and Markdown
- Cache control headers

## Accessing Your Site

After deployment:
- **Production URL:** `https://your-project.vercel.app`
- **Preview URLs:** Created for each deployment

## Viewing Markdown Files

Markdown files (`.md`) will be served as plain text. To view them with formatting:
1. Use a browser extension like "Markdown Viewer"
2. Or access via GitHub if your repo is on GitHub
3. Or convert to HTML (optional enhancement)

## Custom Domain (Optional)

1. Go to your project settings in Vercel dashboard
2. Navigate to "Domains"
3. Add your custom domain
4. Follow DNS configuration instructions

## Troubleshooting

### Issue: Files not loading
- **Solution:** Ensure all HTML files are in the same directory as `index.html`
- Check that file names match exactly (case-sensitive)

### Issue: Markdown files showing as plain text
- **Solution:** This is expected. Use a markdown viewer extension or access via GitHub

### Issue: Large file sizes
- **Note:** HTML files are ~4.6MB each (contain embedded data)
- Vercel supports files up to 50MB, so this is fine
- First load may be slower, but Vercel CDN will cache them

### Issue: 404 errors
- **Solution:** Check that `vercel.json` routing is correct
- Ensure all linked files exist in the project

## Performance Tips

1. **Enable Vercel Analytics** (optional) to monitor performance
2. **Use Vercel's CDN** - files are automatically cached globally
3. **Consider lazy loading** for future enhancements (not needed now)

## Updating Your Site

### Via Git (Recommended):
1. Make changes to files
2. Commit and push to your repository
3. Vercel will automatically redeploy

### Via Vercel Dashboard:
1. Go to your project
2. Use "Redeploy" option
3. Or upload new files via dashboard

## Support

For Vercel-specific issues:
- [Vercel Documentation](https://vercel.com/docs)
- [Vercel Support](https://vercel.com/support)

For project-specific issues:
- Check `README.md` and `VISUALIZATION_GUIDE.md`
- Review file structure matches expected layout

---

**Ready to deploy?** Follow Option 1 above for the fastest setup! 🚀

