/**
 * tw-analytics v0.1.0
 * Lightweight page view analytics for TW Framework
 *
 * Hook: afterBuild
 * Adds a small <script> tag to every built HTML page that logs
 * page views to the console (replace with your endpoint).
 */

module.exports = {
  afterBuild: function(ctx) {
    var pages = ctx.pages || [];
    var snippet = '<script>console.log("[tw-analytics] page view tracked");</script>';
    for (var i = 0; i < pages.length; i++) {
      if (pages[i].html && pages[i].html.indexOf("</body>") !== -1) {
        pages[i].html = pages[i].html.replace("</body>", snippet + "</body>");
      }
    }
    return { modified: true };
  }
};
