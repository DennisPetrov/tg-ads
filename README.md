# Telegram Mini Apps with VOX ad example
This is a basic and straightforward Telegram Mini App(TMA) implemented using plain JavaScript, HTML, and CSS with integrated VOX ad.

## How to integrate VOX simple ad in your TMA

1. Add VOX ssp script in your application footer, before the closing </body> tag:

```
  <script type="text/javascript">
      if (typeof window._tx === "undefined") {
          var s = document.createElement("script");
          s.type = "text/javascript";
          s.async = true;
          s.src = "https://st.hbrd.io/ssp.js?t=" + new Date().getTime();
          (document.getElementsByTagName("head")[0] || document.getElementsByTagName("body")[0]).appendChild(s);
      }
      window._tx = window._tx || {};
      window._tx.cmds = window._tx.cmds || [];
      window._tx.cmds.push(function () {
          window._tx.init();
      });
  </script>
```

2. Add vox placement where you want to show ad:

```
<div data-hyb-ssp-ad-place="000000000000000000000000"></div>
```

3. Replace 000000000000000000000000 with vox placement id. You can get vox placement id from your VOX publisher manager.
Or send us a message here https://voxexchange.io/#CONTACT_US

4. See integration example here:
[Source code](./index.html)
[TMA example](https://t.me/TestVoxPlacementBot)