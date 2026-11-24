---
title: "What I Do"
---
<style>
/* The graphic is laid out at 1600x1200 (the size it was designed at) and
   scaled to fit the box, so it keeps the same 4:3 ratio at any width.
   The script below sets --graphic-scale from the box's actual width. */
.graphic-embed{
  --graphic-scale: .6725;
  width: min(1076px, calc(100vw - 44px));
  aspect-ratio: 1600 / 1200;
  margin: 14px 0 18px;
  border-radius: 14px;
  overflow: hidden;
  box-shadow: 0 0 0 1px var(--border), 0 12px 30px rgba(2,6,23,.12);
  background: var(--bg);
}
.graphic-embed iframe{
  width: 1600px;
  max-width: none;   /* the site's iframe{max-width:100%} would squeeze the layout */
  height: 1200px;
  border: 0;
  display: block;
  transform: scale(var(--graphic-scale));
  transform-origin: 0 0;
}
</style>

I’m the Senior Technical Content Writer at PagerDuty, and a team of one for the company’s customer docs and e-learning content. Click any card in the graphic to see what comes in, what I put out, and the tools that make it work.

<div class="graphic-embed">
<iframe src="graphic/" title="What I do at PagerDuty: interactive graphic" allow="fullscreen" allowfullscreen></iframe>
</div>
<script>
  // Keep the graphic scaled to its box so it holds the same 4:3 ratio at any width.
  (function(){
    document.querySelectorAll('.graphic-embed').forEach(function(box){
      function fit(){ if (box.clientWidth) box.style.setProperty('--graphic-scale', box.clientWidth / 1600); }
      fit();
      if (window.ResizeObserver) new ResizeObserver(fit).observe(box);
      else window.addEventListener('resize', fit);
    });
  })();
</script>

👉 [Open the graphic full size →](graphic/)

### Moving our docs to docs as code

I helped move docs.pagerduty.com off ReadMe.io and onto a GitHub-based Next.js site. The top row shows the migration. The bottom loop shows how every docs change works now, including the check that keeps our product tours and guides up to date. Click any card to learn more.

<div class="graphic-embed" id="migration-embed">
<iframe src="migration/" title="From ReadMe.io to docs as code: interactive graphic" loading="lazy" allow="fullscreen" allowfullscreen></iframe>
</div>
<script>
  (function(){
    var box = document.getElementById('migration-embed');
    function fit(){ if (box.clientWidth) box.style.setProperty('--graphic-scale', box.clientWidth / 1600); }
    fit();
    if (window.ResizeObserver) new ResizeObserver(fit).observe(box);
    else window.addEventListener('resize', fit);
  })();
</script>

👉 [Open the migration graphic full size →](migration/)
