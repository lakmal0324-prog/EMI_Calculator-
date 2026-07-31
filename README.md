# ලීස් ලෙජරය — Lease / EMI Repayment Calculator

Reducing-balance lease/EMI schedule calculator, fixed monthly rental (auto-solved from rate + tenure + balloon payments), with balloon-payment support. Built to match HDFC-style LEF850 lease amortization schedules.

Installable as a home-screen app (PWA) — opens full-screen, no browser address bar, with its own icon.

## 🚀 GitHub Pages එකෙන් host කරන විදිහ

1. **Repo එකක් හදන්න**
   - GitHub එකට login වෙන්න → **New repository**
   - නමක් දෙන්න (උදා: `lease-emi-calculator`)
   - Public කරන්න → **Create repository**

2. **මේ files ඔක්කොම upload කරන්න**
   - `index.html`
   - `manifest.json`
   - `sw.js`
   - `icon-192.png`
   - `icon-512.png`
   - `icon-180.png`
   - `README.md`
   - `LICENSE`
   - Repo page එකේ **Add file → Upload files** එබලා ඔක්කොම දාන්න → **Commit changes**

3. **GitHub Pages ක්‍රියාත්මක කරන්න**
   - Repo එකේ **Settings** → **Pages** (left sidebar) වෙත යන්න
   - **Branch**: `main` (හෝ `master`) සහ folder: `/ (root)` තෝරන්න → **Save**
   - මිනිත්තු කිහිපයකින් ඔබට මෙහෙම link එකක් ලැබෙනවා:
     ```
     https://<your-username>.github.io/<repo-name>/
     ```

4. ඒ link එක open කරලා බලන්න — app එක ready!

## 📱 Real App එකක් වගේ Home Screen එකට Install කරගන්නා විදිහ

**iPhone (Safari):**
1. Link එක Safari එකෙන් open කරන්න
2. පහළ **Share** icon එක (□↑) tap කරන්න
3. **"Add to Home Screen"** තෝරන්න → **Add**
4. දැන් Home Screen එකේ Lease Ledger icon එකක් පේනවා — tap කළොත් full-screen app එකක් වගේ open වෙනවා, Safari address bar එකක් නැතුව

**Android (Chrome):**
1. Link එක Chrome එකෙන් open කරන්න
2. ඉහළ **⋮ menu** → **"Install app"** හෝ **"Add to Home screen"**
3. Confirm කරන්න
4. Icon එකක් Home Screen එකේ පේනවා, app drawer එකේත් පේනවා

මෙතැන් සිට, එය බලද්දී link එකක් වගේ නෙවෙයි, install කරපු app එකක් වගේ පෙනෙනවා.

## 🛠️ වෙනස් කරගන්න ඕන නම්

`index.html` file එකේ HTML/CSS/JS තියෙන්නේ. GitHub එකේම **Edit (pencil icon)** එබලා කෙළින්ම browser එකෙන් වෙනස් කරන්නත් පුළුවන් (commit කළාම automatic ලෙස site එක update වෙනවා).

## ගණනය කරන ක්‍රමය

- සෑම මාසයකටම ස්ථාවර වාරිකයක් අය කෙරේ
- පොලිය = ඉතිරි ශේෂය × (වාර්ෂික අනුපාතය / 12)
- ප්‍රතිපූර්ණය = වාරිකය − පොලිය
- Balloon මාස වලදී, එම මාසයේ මුළු වාරිකයම ඔබ දෙන balloon මුදලින් replace වේ
- Regular rental එක binary-search algorithm එකකින් auto-calculate වේ, එසේ ණය මුදල අවසාන මාසයේදී හරියටම බිංදුවට පත් වේ

