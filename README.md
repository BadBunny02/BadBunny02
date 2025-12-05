<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 250" width="100%" height="250" role="img" aria-labelledby="title desc" data-name="Anupam" data-subtitle="C++ • Python • Linux • Machine Learning">


<!-- right column: text -->
<g transform="translate(160,72)">
<!-- name with gradient stroke + mask sweep -->
<text id="nameText" x="0" y="0" font-family="Inter, system-ui" font-weight="800" font-size="46" fill="url(#textGradient)" paint-order="stroke fill" stroke="#071428" stroke-width="0.6" >
<!-- initial text from data-name attribute will be inserted/updated by JS when embedding as HTML; the README inline SVG can be edited manually. -->
</text>


<!-- subtitle -->
<text id="subText" x="0" y="44" font-family="Inter, system-ui" font-weight="600" font-size="18" fill="#9fb0d9" >
</text>


<!-- descriptive line / tagline -->
<text id="tagText" x="0" y="82" font-family="Inter, system-ui" font-weight="500" font-size="14" fill="#9aa4c0" >
Building tools, systems & learning by breaking things.
</text>


</g>


<!-- big subtle code-like block at right to balance composition -->
<g transform="translate(600,36)">
<rect x="0" y="0" width="320" height="178" rx="12" ry="12" fill="#031226" stroke="#0b2540" />
<!-- few lines -->
<rect x="18" y="18" width="250" height="12" rx="6" fill="#071a2f" />
<rect x="18" y="40" width="220" height="10" rx="5" fill="#071a2f" />
<rect x="18" y="60" width="190" height="10" rx="5" fill="#071a2f" />
<rect x="18" y="82" width="240" height="10" rx="5" fill="#071a2f" />


<!-- small animated caret -->
<rect x="22" y="108" width="8" height="14" fill="url(#textGradient)">
<animate attributeName="y" values="108;104;108" dur="1.2s" repeatCount="indefinite" />
</rect>
</g>


<!-- accessible focus rect (hidden visually) for screen readers when embedded as standalone -->
<rect x="0" y="0" width="100%" height="100%" fill="transparent" />


<!-- JavaScript-driven text insertion only used in preview HTML (ignored if SVG is embedded standalone in README) -->
<script type="application/ecmascript"><![CDATA[
(function(){
try {
// Respect reduced motion
var reduced = window.matchMedia && window.matchMedia('(prefers-reduced-motion: reduce)').matches;
if (reduced) {
// stop SMIL animations by removing animate elements
var anims = document.querySelectorAll('animate, animateTransform');
anims.forEach(function(a){ a.parentNode && a.parentNode.removeChild(a); });
}


var svg = document.currentScript.ownerDocument.querySelector('svg');
if (!svg) return;
// get name & subtitle from data attributes on svg
var name = svg.getAttribute('data-name') || 'Anupam';
var subtitle = svg.getAttribute('data-subtitle') || 'C++ • Python • Linux • Machine Learning';


// insert into text nodes (supports unicode)
var nameText = svg.getElementById('nameText');
var subText = svg.getElementById('subText');
if (nameText) {
// create tspan to allow wrapping if name too long
var tspan = document.createElementNS('http://www.w3.org/2000/svg','tspan');
tspan.setAttribute('x',0);
tspan.setAttribute('dy','0');
tspan.textContent = name;
nameText.appendChild(tspan);


// add a soft animated glow by duplicating the text as a blurred fill (only in HTML preview)
var clone = nameText.cloneNode(true);
clone.setAttribute('fill','none');
clone.setAttribute('stroke','rgba(255,255,255,0.06)');
clone.setAttribute('stroke-width','12');
clone.setAttribute('filter','url(#softShadow)');
nameText.parentNode.insertBefore(clone, nameText);
}
if (subText) subText.textContent = subtitle;


// helper: if someone wants to edit text dynamically via query string ?name=...
var params = new URLSearchParams(location.search);
if (params.get('name')) {
nameText.textContent = params.get('name');
}
if (params.get('subtitle')) {
subText.textContent = params.get('subtitle');
}
} catch (e){ console.warn('SVG banner init error', e); }
})();
]]></script>


</svg>
