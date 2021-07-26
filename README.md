<p align="center">
  <a href="http://lovera.maxam.now.sh/">
    <img src="https://user-images.githubusercontent.com/25841814/79395484-5081ae80-7fac-11ea-9e27-ac91472e31dd.png" alt="screenshot" width="500">
  </a>
  <h3 align="center">📌✨productive-box</h3>
</p>

<p align="center">
   <img src="https://img.shields.io/badge/language-typescript-blue?style"/>
   <img src="https://img.shields.io/github/license/maxam2017/productive-box"/>
   <img src="https://img.shields.io/github/stars/maxam2017/productive-box"/>
   <img src="https://img.shields.io/github/forks/maxam2017/productive-box"/>
</p>
<p align="center">
   Are you an early 🐤 or a night 🦉?
   <br/>
   When are you most productive during the day?
   <br/>
   Let's check out in gist!
</p>

---

> This project is inspired by an awesome pinned-gist project.<br/>Find more in https://github.com/matchai/awesome-pinned-gists

## Overview
This project uses GitHub graphQL API to get the commit histories and write into the gist by [rest.js](https://github.com/octokit/rest.js#readme)

## Setup

### Prep work
1. Create a new public GitHub Gist (https://gist.github.com/)
1. Create a token with the `gist` and `repo` scope and copy it. (https://github.com/settings/tokens/new)
   > enable `repo` scope seems **DANGEROUS**<br/>
   > but this GitHub Action only accesses your commit timestamp in repository you contributed.

### Project setup

1. Fork this repo
1. Open the "Actions" tab of your fork and click the "enable" button
1. Edit the [environment variable](https://github.com/maxam2017/productive-box/blob/master/.github/workflows/schedule.yml#L17-L18) in `.github/workflows/schedule.yml`:

   - **GIST_ID:** The ID portion from your gist url: `https://gist.github.com/maxam2017/`**`9842e074b8ee46aef76fd0d493bae0ed`**.
   - **TIMEZONE:** The timezone of your location, eg. `Asia/Taipei` for Taiwan, `America/New_York` for America in New York, etc.

1. Go to the repo **Settings > Secrets**
1. Add the following environment variables:
   - **GH_TOKEN:** The GitHub token generated above.
1. [Pin the newly created Gist](https://help.github.com/en/github/setting-up-and-managing-your-github-profile/pinning-items-to-your-profile)


## Setup(Korean)

### 사전 작업

1. https://gist.github.com/ 에서 **public** 으로 신규 gist를 생성

  제목과 내용은 나중에 자동으로 업데이트 된다. 일단 아무 내용이나 작성해 놓기

2. [github 토큰 생성](https://github.com/settings/tokens/new) 페이지에서 **gist**와 **repo** scope를 활성화해 token을 발급

  이 때 발급된 토큰은 페이지를 빠져나가면 다시 얻을 수 없으므로 클립보드 등에 저장해 두기


### 라이브러리 사용

1. [productive-box](https://github.com/maxam2017/productive-box) repository를 fork!

2. fork 된 내 repository의 **Action** 탭에서 **enabled** 버튼을 눌러 Action을 활성화

3. **.github/workflow/Schedule.yml** 파일을 수정해 환경변수 작성
  - GIST_ID: 사전작업 1번 step에서 생성된 gist의 id
  - TIMEZONE: **Asia/Seoul**

4. **Settings 탭 > Secrets**에 접속해서 **New repository secret** 버튼 클릭해 환경변수 설정
  - GH_TOKEN: 사전작업 2번 step에서 발급받은 토큰

5. [gist를 내 프로필에 고정](https://docs.github.com/en/github/setting-up-and-managing-your-github-profile/customizing-your-profile/pinning-items-to-your-profile)

6. Action 주기(1시간)에 따라 자동으로 갱신. 즉시 적용하고 싶다면 **README.me** 파일을 수정하는 등 파일에 변화를 주면 즉시 적용된다.








