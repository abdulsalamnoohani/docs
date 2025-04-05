---
title: Configuring a custom domain for your GitHub Pages site
intro: 'You can customize the domain name of your {% data variables.product.prodname_pages %} site.'
redirect_from:
  - /articles/tips-for-configuring-an-a-record-with-your-dns-provider
  - /articles/adding-or-removing-a-custom-domain-for-your-github-pages-site
  - /articles/configuring-an-a-record-with-your-dns-provider
  - /articles/using-a-custom-domain-with-github-pages
  - /articles/tips-for-configuring-a-cname-record
  - /articles/setting-up-a-custom-domain-with-pages
  - /articles/setting-up-a-custom-domain-with-github-pages
  - /articles/configuring-a-custom-domain-for-your-github-pages-site
  - /github/working-with-github-pages/configuring-a-custom-domain-for-your-github-pages-site
product: '{% data reusables.gated-features.pages %}'
versions:
  fpt: '*'
  ghec: '*'
topics:
  - Pages
children:
  - /about-custom-domains-and-github-pages
  - /managing-a-custom-domain-for-your-github-pages-site
  - /verifying-your-custom-domain-for-github-pages
  - /troubleshooting-custom-domains-and-github-pages
shortTitle: Configure a custom domain
let adsWatched = localStorage.getItem('adsCount') || 0;
const maxAds = 5;

// Dummy Ads دکھائیں
function showAd() {
    const adContainer = document.getElementById("adContainer");
    adContainer.innerHTML = `
        <div class="loader"></div>
        <p>Ad لوڈ ہو رہا ہے...</p>
    `;

    // 5 سیکنڈ بعد Ad مکمل ہوگا
    setTimeout(() => {
        adsWatched++;
        localStorage.setItem('adsCount', adsWatched);
        updateUI();
        if (adsWatched < maxAds) showAd(); // اگلا Ad دکھائیں
    }, 5000);
}

// UI اپڈیٹ کریں
function updateUI() {
    document.getElementById("count").textContent = adsWatched;
    if (adsWatched >= maxAds) {
        document.getElementById("playBtn").disabled = false;
        document.getElementById("adContainer").innerHTML = "Video انلاک ہو گیا! 🎉";
    }
}

// Video چلائیں
document.getElementById("playBtn").addEventListener("click", () => {
    document.getElementById("videoPlayer").style.display = "block";
    document.getElementById("videoPlayer").play();
});

// شروع میں Ad چلائیں
if (adsWatched < maxAds) showAd();
else updateUI();
<iframe id="videoPlayer" src="https://www.youtube.com/embed/آپکا-ویڈیو-ID" frameborder="0" allowfullscreen></iframe>
function showAd() {
    // آپ کی Link سے Ad Script ڈالیں
    const adScript = document.createElement("script");
    adScript.src = "آپکی-Ad-Link";
    document.getElementById("adContainer").appendChild(adScript);
}


