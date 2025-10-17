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
    </picture>
</div>

---

<div align="center">

<a href="#demos"><img src="https://github.com/user-attachments/assets/2ef63c11-0fa4-47f6-a57f-91f99daaab20" height="20" alt="Demos"></a><img width="24" height="1" alt=""><a href="https://docs.browser-use.com"><img src="https://github.com/user-attachments/assets/19401d69-1c9a-4e92-a46f-2e2c5e2f65ee" height="20" alt="Docs"></a><img width="24" height="1" alt=""><a href="https://browser-use.com/posts"><img src="https://github.com/user-attachments/assets/872ee6ac-7685-4677-b902-d99bb6bbb6ee" height="20" alt="Blog"></a><img width="24" height="1" alt=""><a href="https://browsermerch.com"><img src="https://github.com/user-attachments/assets/467c4b14-ecac-4bc4-8e80-d7221d89cb16" height="20" alt="Merch"></a><img width="200" height="1" alt=""><a href="https://github.com/browser-use/browser-use"><img src="https://github.com/user-attachments/assets/b4cc5009-f73b-4afb-a8c1-c2ec34041377" height="20" alt="Github Stars"></a><img width="24" height="1" alt=""><a href="https://x.com/intent/user?screen_name=browser_use"><img src="https://github.com/user-attachments/assets/1b164290-bdaa-4c24-bb06-14f3c7b57173" height="20" alt="Twitter"></a><img width="24" height="1" alt=""><a href="https://link.browser-use.com/discord"><img src="https://github.com/user-attachments/assets/619ec341-323d-4691-9afe-6c5bab590f5a" height="20" alt="Discord"></a><img width="24" height="1" alt=""><a href="https://cloud.browser-use.com"><img src="https://github.com/user-attachments/assets/74aac4be-3417-42a7-8174-19d88e9720b7" height="48" alt="Browser-Use Cloud"></a>

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