<!--
version:  0.0.1
language: de
narrator: Deutsch Female

@onload
(function () {

  // =========================
  // Init (pro Dokument nur einmal)
  // =========================
  const KEY = "__LIA_DIKTAT_AUTOWIDTH_V1__";
  if (window[KEY]) return;
  window[KEY] = true;

  // =========================
  // CSS Injection (statt @style)
  // =========================
  const STYLE_ID = "lia-diktat-css-v1";
  if (!document.getElementById(STYLE_ID)) {
    const css = `
.lia-diktat{
  display:inline-block;
  vertical-align:baseline;
  max-width:100%;
}

/* egal welchen Wrapper LiaScript um [[...]] baut: inline halten */
.lia-diktat > :not(.lia-diktat-measure){
  display:inline-block !important;
  vertical-align:baseline;
}

/* robust gegen zusätzliche Wrapper */
.lia-diktat :where(div,span){
  vertical-align:baseline;
}
.lia-diktat :where(div,span):not(.lia-diktat-measure){
  display:inline-block !important;
}

.lia-diktat input,
.lia-diktat textarea{
  display:inline-block !important;
  vertical-align:baseline;
  box-sizing:border-box;
  max-width:100%;
}
    `.trim();

    const st = document.createElement("style");
    st.id = STYLE_ID;
    st.textContent = css;
    (document.head || document.documentElement).appendChild(st);
  }

  // =========================
  // Auto-Fit Logik
  // =========================
  const num = (v) => {
    const x = parseFloat(v);
    return Number.isFinite(x) ? x : 0;
  };

  function fitOne(wrapper){
    const meas  = wrapper.querySelector(".lia-diktat-measure");
    const input = wrapper.querySelector("input, textarea");
    if(!meas || !input) return false;

    const cs = getComputedStyle(input);
    meas.style.font = cs.font;
    meas.style.letterSpacing = cs.letterSpacing;
    meas.style.textTransform = cs.textTransform;

    const textW = meas.getBoundingClientRect().width;
    const pad   = num(cs.paddingLeft) + num(cs.paddingRight);
    const bord  = num(cs.borderLeftWidth) + num(cs.borderRightWidth);

    const w = Math.ceil(textW + pad + bord + 14); // Cursor/Luft

    input.style.minWidth = "6ch";
    input.style.width    = w + "px";
    input.style.maxWidth = "100%";
    return true;
  }

  let scheduled = false;
  function fitAll(){
    if (scheduled) return;
    scheduled = true;
    requestAnimationFrame(() => {
      scheduled = false;
      document.querySelectorAll(".lia-diktat").forEach(w => {
        let tries = 0;
        (function retry(){
          if (fitOne(w)) return;
          if (tries++ < 60) requestAnimationFrame(retry);
        })();
      });
    });
  }

  if (document.readyState === "loading") {
    document.addEventListener("DOMContentLoaded", fitAll, { once:true });
  } else {
    fitAll();
  }

  window.addEventListener("resize", fitAll);
  if (document.fonts && document.fonts.ready) document.fonts.ready.then(fitAll);

  const mo = new MutationObserver(() => fitAll());
  mo.observe(document.body, { childList:true, subtree:true });

})();
@end


@diktat: @diktat_(@uid,@0)

@diktat_
<span class="lia-diktat" id="lia-diktat-@0">{|>}{<span class="lia-diktat-measure" style="position:absolute;left:-10000px;top:auto;width:auto;height:auto;overflow:hidden;white-space:pre;">@1</span>}[[ @1 ]]</span>
@end
-->



# Dann schauen wir mal




@diktat(Ein Vogel fliegt hoch über den stillen See.)








Anna ging in einen @diktat(Zoo). Dort konnte sie auf einem @diktat(Lama) reiten.

