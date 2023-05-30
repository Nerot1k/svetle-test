<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="utf-8" />
		<link rel="icon" href="./favicon.png" />
		<meta name="viewport" content="width=device-width" />
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
		
		<link href="./_app/immutable/assets/_layout.65099de4.css" rel="stylesheet">
		<link href="./_app/immutable/assets/_page.49704240.css" rel="stylesheet">
	</head>
	<body data-sveltekit-preload-data="hover">
		<div style="display: contents">


<nav><div class="nav-container"><a href="/" class="nav-logo" title="Back to Homepage">Тушалиев Артём</a>
        <div class="nav-links"><a href="/about" class="link">Обо мне</a><a href="/blog" class="link">Блог</a><a href="/project" class="link">Портфолио</a><a href="/contact" class="link">Контакты</a></div></div></nav>

<div class="container svelte-1m8mvlz">
    <h1>Контакты</h1>

<div class="svelte-1wltilb"><ul><li>Email: [email]</li>
		<li>Телефон: [номер телефона]</li>
		<li>Адрес: [адрес]</li></ul>

	<p class="svelte-1wltilb">Я всегда открыт для общения. Не стесняйтесь написать мне или позвонить.</p></div>
<div class="svelte-1wltilb"><ul><li>Вконтакте: [Вконтакте аккаунт]</li>
		<li>Одноклассники: [Одноклассники аккаунт]</li>
		<li>Дзен: [Дзен аккаунт]</li></ul>

	<p class="svelte-1wltilb">Я буду рад видеть вас в своих контактах и готов настроить полезные и
		продуктивные отношения. Если вы заинтересованы в сотрудничестве, я всегда
		готов обсудить возможности и принять участие в вашем проекте.
	</p>
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
	</body>
</html>