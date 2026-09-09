SEASONAL FORECASTS — GITHUB PAGES SETUP

This package contains index.html and your two original logos. The 30 forecast
maps are NOT included: copy your PNG files into the images folder.

1. Extract seasonal-forecasts.zip on your computer.
2. Copy all 30 forecast PNGs into seasonal-forecasts/images without renaming them.
3. Double-click index.html to check the page locally. No installation is needed.
4. On https://github.com/new create a public repository named seasonal-forecasts
   under GeorgeMJ23. Select Add a README to initialize the main branch.
5. In that repository select Add file > Upload files. Drag the CONTENTS of the
   extracted seasonal-forecasts folder (index.html, logos, images, README.txt)
   into the upload area. Do not upload the ZIP or its outer folder. Keep the
   logos and images folders intact. Commit the uploaded files to main; if you
   use a pull request, merge it so the files are present on main.
6. Open Settings > Pages. Under Build and deployment choose:
      Source: Deploy from a branch
      Branch: main
      Folder: / (root)
   Click Save. After publication, GitHub Pages displays your live site link.
7. With that exact repository name, the expected address is:
   https://georgemj23.github.io/seasonal-forecasts/

GitHub web uploads support up to 100 files at once, each no larger than 25 MiB.
If a map exceeds that size, use GitHub Desktop/Git (normal Git files, not LFS)
or reduce its PNG size. For this small collection, ordinary repository files
are appropriate, provided overall GitHub Pages limits are respected.

BEHAVIOR
- Initial view: precipitation, September 2026.
- Changing the variable immediately selects its September map.
- Left/right buttons select consecutive months. They stop at the endpoints.
- January and February are in 2027, but ALL filenames still end in _202609.png
  because this identifies the September 2026 forecast initialization.
- Maps retain their full aspect ratio: no cropping or changes to the data.
- If a file is absent, the page shows an unavailable message.

EXPECTED FILENAMES
For each of these variable codes:
  mm                      Precipitation
  MSLP                    Mean sea level pressure
  Snowfall-Precipitation   Snowfall
  T2m                     Temperature
  Z500                    Geopotential height at 500 hPa
the page expects:
  ECMWF_CODE_LT1_September_202609.png
  ECMWF_CODE_LT2_October_202609.png
  ECMWF_CODE_LT3_November_202609.png
  ECMWF_CODE_LT4_December_202609.png
  ECMWF_CODE_LT5_January_202609.png
  ECMWF_CODE_LT6_February_202609.png
Replace CODE with each exact code above. Capitalization matters on GitHub Pages.
Example: images/ECMWF_Snowfall-Precipitation_LT6_February_202609.png

UPDATING MAPS
For corrections to this forecast, upload replacement images with the same names.
GitHub Pages republishes changes committed to the publishing branch.
For a new initialization, edit FORECAST_RUN and MONTHS in index.html, as well
as the visible edition text, description metadata, and image alt initialization.
Then upload the new matching PNGs.

OFFICIAL GITHUB HELP
https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
https://docs.github.com/en/repositories/working-with-files/managing-files/adding-a-file-to-a-repository
