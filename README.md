# AskGPT

<a href="https://www.producthunt.com/posts/askgpt-an-alfred-workflow?utm_source=badge-featured&utm_medium=badge&utm_souce=badge-askgpt&#0045;an&#0045;alfred&#0045;workflow" target="_blank"><img src="https://api.producthunt.com/widgets/embed-image/v1/featured.svg?post_id=385969&theme=light" alt="AskGPT&#0058;&#0032;An&#0032;Alfred&#0032;Workflow - Ask&#0032;ChatGPT&#0032;from&#0032;anywhere&#0032;while&#0032;typing | Product Hunt" style="width: 250px; height: 54px;" width="250" height="54" /></a>

This is an **Alfred Workflow** that enables you to ask **ChatGPT** from anywhere while typing. With this Workflow, you can activate it in any window just by typing `\\gpt`, and it will swiftly generate the content you desire based on your commands. It's like having a genie in a bottle that instantly fulfills your commands!

---

<img src="https://user-images.githubusercontent.com/10487750/227745921-6d163359-f660-4ec7-9856-dd67dd8a8034.png"  width="30%" height="30%" alt="A man with his feet on the table, looking at automatically generated program code, cyberpunk">

by DALL·E *"A man with his feet on the table, looking at automatically generated program code, cyberpunk"*

## Getting Start

- Make sure you are using **Alfred 5** (Try [v0.5](https://github.com/phguo/AskGPT/releases/tag/v0.5) if you use Alfred 4).
- Make sure Alfred 5 has been granted in "System Preferences -> Security & Privacy -> Privacy Tab -> Accessibility".
- Download and install "AskGPT" from https://github.com/phguo/AskGPT/releases.
- Set the required Environment Variables (click the top-right [x] icon):
  - `API_KEY`: obtain one from https://platform.openai.com/account/api-keys.
  - `PYTHON_ENV`: it will be like `/Users/<user_name>/miniconda3/bin/python` if you follow the following steps.
      - Install Python from https://docs.conda.io/en/latest/miniconda.html.
      - Install the required Python packages by `pip install openai keyboard pyperclip`.
  - `API_BASE`: it will be like https://..**/v1 write your own openai api proxy url(default:https://api.openai.com/v1)
- To make `\\gpt` work, see [#6](https://github.com/phguo/AskGPT/issues/6#issuecomment-1509431313).

__* This project has only been tested on macOS Monterey 12.6.3.__ Please feel free to report any issues such as bugs or feature recommendations.

## Usage

<img src="https://github.com/phguo/AskGPT/blob/main/video/alfred.png"  width="60%" height="60%">


You can access the Workflow by Alfred keyword `gpt` or typing `\\gpt` anywhere. The following are some use cases.

Let AskGPT write an email for you:

![email](https://github.com/phguo/AskGPT/blob/main/video/email.gif)

Let AskGPT write code for you:

![hello](https://github.com/phguo/AskGPT/blob/main/video/hello.gif)

Let AskGPT check grammar errors (from clipboard) for you:

![grammar](https://github.com/phguo/AskGPT/blob/main/video/grammar.gif)

## Changelog

[v0.6.1](https://github.com/phguo/AskGPT/releases/tag/v0.6.1) - Apr. 4, 2023
  - Fix [#5](https://github.com/phguo/AskGPT/issues/5) that are related to the roles parser.
  - Add a configuration for printing user-inputted content.

[v0.6](https://github.com/phguo/AskGPT/releases/tag/v0.6) - Apr. 2, 2023

<img src="https://raw.githubusercontent.com/phguo/AskGPT/main/video/v0.6_User_Configuration.png"  width="70%" height="70%">

  - Support context.
  - Support user defined `model` and `temprature`.
  - Support user defined `roles`.
  - Move configuration except `API_KEY` and `PYTHON_ENV` to Alfred 5's [User Configuration](https://www.alfredapp.com/help/workflows/user-configuration/) page.

[v0.5](https://github.com/phguo/AskGPT/releases/tag/v0.5) - Mar. 26, 2023
  - The first release.
  - Activate by Alfred keyword `gpt`.
  - Activete by typing `\\gpt` anywhere.
  - Access clipbord content by "`clip`".

## TODO

- [ ] Detect invalid configuration
- [ ] Automaticly update of the Workflow
- [ ] Terminate output when the window you are using is changed
- [x] **[v0.6](https://github.com/phguo/AskGPT/releases/tag/v0.6)**, Preserve context (number of problems, delay in time, manually release, suggested by [tommyxps](https://www.v2ex.com/t/927205#r_12870341))
- [x] **[v0.6](https://github.com/phguo/AskGPT/releases/tag/v0.6)**, Save customized prompt (suggested by [tommyxps at Product Hunt](https://www.producthunt.com/posts/askgpt-an-alfred-workflow?comment=2314975))

## License

This project is licensed under the MIT License, see the [LICENSE](https://github.com/phguo/AskGPT/blob/main/LICENSE) file for details.

## Acknowledgments

- This project was inspired by [AnyGPT](https://www.producthunt.com/posts/anygpt).
- The predefined role `*polish: Revise the following sentences to make them more clear, concise, and coherent.` was designed by [reycn](https://github.com/yetone/bob-plugin-openai-polisher/pull/2) for [yetone/bob-plugin-openai-polisher](https://github.com/yetone/bob-plugin-openai-polisher).

---

☕️ Consider buy me a coffee if you find it helpful: https://guoph.gumroad.com/l/askgpt
