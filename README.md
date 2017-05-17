# Roots Bedrock support for WPEngine
WPEngine doesn't support Composer, Gulp or Bower. This bash script will move the `app/` folder back to 'wp-content/'. It will update the root .gitignore (and clear the cache) so all files are ignored, except those in the `wp-content/` folder. It will then remove any .git related files in the wp-content/ folder so submodules and compiled assets are included. Finally, it will push up the branch to WPEngine (replacing capistrano). This is all completed on a separate WPEngine branch which is created initially and deleted after completion.

# Usage
1. Edit the name of the theme in `wpengine.sh`
2. Ensure you use develop branch for staging, master for production locally
3. Ensure you use staging, production remotes for WPEngine
4. Run `sh wpengine.sh` followed by `staging` or `production`. E.g `sh wpengine.sh staging`

# Customisation
1. line 4: commented the theme		// Because we will be using our custom theme everytime 
2. lin3 36: "bedrock"				// This is the installed directory of wordpress that contains all files.
3. line 39 to 58 commented			// Because we will be using our custom theme everytime
