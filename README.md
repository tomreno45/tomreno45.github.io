# 🏈 WFL Team Manager

A pure static web application for managing WFL team data. Runs entirely in the browser using JavaScript and SQL.js - no server required!

## ✨ Features

- 📊 **Team Rosters** - View complete player rosters with stats
- 🏆 **Standings** - Real-time team rankings
- 📈 **Season Stats** - Player statistics by skill category
- 🗞️ **WFL News** - Twitter-style news feed
- 🎨 **Team Logos** - Visual branding throughout
- 📱 **Responsive Design** - Works on all devices
- ⚡ **100% Static** - No backend server needed!



### Update Database
1. Replace `GameTest.db` with your new database
2. Commit and push:
```bash
git add GameTest.db
git commit -m "Update database"
git push
```
3. GitHub Pages will auto-update in 1-2 minutes



Your `GameTest.db` must have these tables:
- `Teams` - Team information
- `Players` - Player data
- `Rosters` - Team rosters
- `PlayerAttributes` - Player ratings (with `overall_let`, `potential_let` columns)
- `GameLog` - Game results
- `SeasonStats` - Player stats per game
- `NewsFeed` - News articles (with `ProfilePicture`, `Media` columns)


To test locally:

1. Start a local web server (required for CORS):
```bash
# Python 3
python -m http.server 8000

# OR Node.js
npx serve
```

2. Open browser to `http://localhost:8000`

**Note:** Can't just open `index.html` directly - browsers block loading `.db` files without a web server.

## ⚠️ Important Notes

- Database loads on page load (~1-5 MB = ~1-2 seconds)
- All processing happens in browser (private and secure)
- No data is sent to any server
- Works offline after first load (browser cache)

## 📊 Database Size Limits

- GitHub Pages: No hard limit, but keep under 100MB per file
- Recommended: Keep database under 50MB for best performance
- Larger databases take longer to load initially

## 🎯 Best Practices

1. **Compress your database** - Remove unused tables/data
2. **Optimize images** - Compress PNGs before uploading
3. **Use GitHub releases** - For versioning different seasons
4. **Branch for development** - Keep `main` branch stable

