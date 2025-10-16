<picture>
  <source media="(prefers-color-scheme: light)" srcset="https://github.com/user-attachments/assets/2ccdb752-22fb-41c7-8948-857fc1ad7e24"">
  <source media="(prefers-color-scheme: dark)" srcset="https://github.com/user-attachments/assets/774a46d5-27a0-490c-b7d0-e65fcbbfa358">
  <img alt="Shows a black Browser Use Logo in light color mode and a white one in dark color mode." src="https://github.com/user-attachments/assets/774a46d5-27a0-490c-b7d0-e65fcbbfa358"  width="full">
</picture>

<div align="center">
    <picture>
    <source media="(prefers-color-scheme: light)" srcset="https://github.com/user-attachments/assets/9955dda9-ede3-4971-8ee0-91cbc3850125"">
    <source media="(prefers-color-scheme: dark)" srcset="https://github.com/user-attachments/assets/6797d09b-8ac3-4cb9-ba07-b289e080765a">
    <img alt="The AI browser agent." src="https://github.com/user-attachments/assets/6797d09b-8ac3-4cb9-ba07-b289e080765a"  width="400">
    </picture>4
</div>

---

<div align="center">
Demos

[![Docs](https://img.shields.io/badge/Docs-📕-blue?style=for-the-badge)](https://docs.browser-use.com)

Blog

[![Merch store](https://img.shields.io/badge/Merch_store-👕-blue)](https://browsermerch.com)

DATE-TIME

STARS
[![Weave Badge](https://img.shields.io/endpoint?url=https%3A%2F%2Fapp.workweave.ai%2Fapi%2Frepository%2Fbadge%2Forg_T5Pvn3UBswTHIsN1dWS3voPg%2F881458615&labelColor=#EC6341)](https://app.workweave.ai/reports/repository/org_T5Pvn3UBswTHIsN1dWS3voPg/881458615)
[![Twitter Follow](https://img.shields.io/twitter/follow/browser_use?style=social)](https://x.com/intent/user?screen_name=browser_use)
[![Discord](https://img.shields.io/discord/1303749220842340412?color=7289DA&label=Discord&logo=discord&logoColor=white)](https://link.browser-use.com/discord)

[![Browser-use cloud](https://img.shields.io/badge/Browser_Use_Cloud-☁️-blue?style=for-the-badge&logo=rocket&logoColor=white)](https://cloud.browser-use.com)
</div>

<div align="center">

<!-- Keep these links. Translations will automatically update with the README. -->
[Deutsch](https://www.readme-i18n.com/browser-use/browser-use?lang=de) |
[Español](https://www.readme-i18n.com/browser-use/browser-use?lang=es) |
[français](https://www.readme-i18n.com/browser-use/browser-use?lang=fr) |
[日本語](https://www.readme-i18n.com/browser-use/browser-use?lang=ja) |
[한국어](https://www.readme-i18n.com/browser-use/browser-use?lang=ko) |
[Português](https://www.readme-i18n.com/browser-use/browser-use?lang=pt) |
[Русский](https://www.readme-i18n.com/browser-use/browser-use?lang=ru) |
[中文](https://www.readme-i18n.com/browser-use/browser-use?lang=zh)

</div>

</br>

# 🤖 LLM Quickstart

1. Clone this repo
2. Direct your favorite coding agent (Cursor, ClaudeS, etc) to [Agents.md](https://docs.browser-use.com/llms-full.txt)
3. Prompt away!

<br/>

# 👋 Human Quickstart

**1. Create environment with [uv](https://docs.astral.sh/uv/) (Python>=3.11):**
```bash
uv venv --python 3.12
source .venv/bin/activate
```

**2. Install Browser-Use package:**
```bash
#  We ship every day - use the latest version!
uv pip install browser-use
```

**3. Get your API key from [Browser Use Cloud](https://cloud.browser-use.com/dashboard/api) and add it to your `.env` file (new signups get $10 free credits):**
```
# .env
BROWSER_USE_API_KEY=your-key
```

**4. Download chromium using playwright's shortcut:**
```bash
uvx playwright install chromium --with-deps --no-shell
```

**5. Run your first agent:**
```python
from browser_use import Agent, ChatBrowserUse

agent = Agent(
    task="Find the number of stars of the browser-use repo",
    llm=ChatBrowserUse(),
)
agent.run_sync()
```

Check out the [library docs](https://docs.browser-use.com) for more!

<br/>

# Stealth Browser Infrastructure

Want to bypass anti-bot detection or run a fleet of agents on the cloud? Use our hosted stealth browsers.

**Follow steps 1-3 above, and pass in a Browser made with the `use_cloud` parameter.**
```python
from browser_use import Agent, Browser, ChatBrowserUse

browser = Browser(
    use_cloud=True,  # Automatically provisions a cloud browser
)
agent = Agent(
    task="Find the number of stars of the browser-use repo",
    llm=ChatBrowserUse(),
    browser=browser,
)
agent.run_sync()
```

**Optional: Follow the link in the console to watch the remote browser.**

Check out the [cloud docs](https://docs.cloud.browser-use.com) for more!

<br/>

# Demos

[Task](https://github.com/browser-use/browser-use/blob/main/examples/use-cases/shopping.py): Add grocery items to cart, and checkout.

[![AI Did My Groceries](https://github.com/user-attachments/assets/a0ffd23d-9a11-4368-8893-b092703abc14)](https://www.youtube.com/watch?v=L2Ya9PYNns8)

<br/>


[Task](https://github.com/browser-use/browser-use/blob/main/examples/use-cases/find_and_apply_to_jobs.py): Read my CV & find ML jobs, save them to a file, and then start applying for them in new tabs, if you need help, ask me.

![Job Application Demo](https://github.com/user-attachments/assets/57865ee6-6004-49d5-b2c2-6dff39ec2ba9)

See [more examples](https://docs.browser-use.com/examples) and give us a star!

<br/>

## 📖 Integrations, hosting, custom tools, MCP, and more on our [Docs ↗](https://docs.browser-use.com)

<br/>

<div align="center">
  
**Tell your computer what to do, and it gets it done.**

<img src="https://github.com/user-attachments/assets/06fa3078-8461-4560-b434-445510c1766f" width="400"/>

[![Twitter Follow](https://img.shields.io/twitter/follow/Magnus?style=social)](https://x.com/intent/user?screen_name=mamagnus00)
&emsp;&emsp;&emsp;
[![Twitter Follow](https://img.shields.io/twitter/follow/Gregor?style=social)](https://x.com/intent/user?screen_name=gregpr07)

</div>

<div align="center"> Made with ❤️ in Zurich and San Francisco </div>