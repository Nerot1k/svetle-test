<style>
    body {
      background-position: left top;
      font-family: "Inter", sans-serif;
      margin: 0;
      background-repeat: no-repeat;
    }

    * {
      box-sizing: border-box;
    }

    a {
      text-decoration: none;
      color: black;
    }

    nav {
      position: sticky;
      top: 0;
      left: 0;
      right: 0;
      margin: 0 80px 0 80px;
      padding-top: 2rem;
      padding-bottom: 2rem;
    }

    nav .nav-container {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .nav-links {
      display: flex;
      justify-content: flex-end;
      align-items: center;
      margin: -1em 0;
      flex: 1 0 auto;
    }

    .nav-links .link {
      position: relative;
      margin: 1em;
      font-size: 0.85rem;
      letter-spacing: 1px;
      color: black;
    }

    .nav-logo {
      position: relative;
      line-height: 1;
      font-size: 1.1rem;
      color: black;
    }
  </style>
<div style="display: contents">

<div class="container svelte-1m8mvlz">
<h1>Контакты</h1>

<div class="svelte-1wltilb"><ul><li>Email: [email]</li>
<li>Телефон: [номер телефона]</li>
<li>Адрес: [адрес]</li>
<li>Вконтакте: [Вконтакте аккаунт]</li></ul>


</div>
</div>


    
    <script>
        {
            __sveltekit_to3qk8 = {
                base: new URL(".", location).pathname.slice(0, -1),
                env: {}
            };

            const element = document.currentScript.parentElement;

            const data = [null,null];

            Promise.all([
                import("./_app/immutable/entry/start.1ee0651f.js"),
                import("./_app/immutable/entry/app.73eb89e8.js")
            ]).then(([kit, app]) => {
                kit.start(app, element, {
                    node_ids: [0, 13],
                    data,
                    form: null,
                    error: null
                });
            });
        }
    </script>
</div>
