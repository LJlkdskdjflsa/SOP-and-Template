- 跟 Sun 要求加入 公司的 Github Report
- 創 gitlab 帳號
  - https://gitlab.xrex.works/users/sign_in
- Mac 設定
  - [[Terminal] 使用 Zsh + Zim + Powerlevel10k 打造美觀又快速的 Terminal](https://raymond102033.medium.com/terminal-setting-by-iterm2-zsh-zim-powerlevel10k-e8c296099142)
  - Install
    - Postman
    - K8slens
    - [MySQL on Docker](https://ithelp.ithome.com.tw/articles/10272193)
- Github 設定
  - [【Git】使用 SSH 金鑰與 GitHub 連線](https://cynthiachuang.github.io/Generating-a-Ssh-Key-and-Adding-It-to-the-Github/)
```
aws eks --region ap-northeast-1 update-kubeconfig --name fasterdev --profile xrex-fasterdev
//
https://github.com/xrex-inc/onboarding/blob/develop/docs/dev_env/fasterdev.md
//
https://github.com/xrex-inc/onboarding
//
[profile xrex-fasterdev]
source_profile=default
role_arn=arn:aws:iam::868121646105:role/Backend
mfa_serial=arn:aws:iam::072020267081:mfa/Simon
duration_seconds=43200
//
[profile default]
region=ap-northeast-1
```
- 嘗試跑第一個服務
  - exchange-market-pool
    - read the structure
    - create `.env`
    - git clone
      - xcode-select --install
   
## 常用面板
### fasterdev
- fasterdev jenkins: https://jenkins-master.xrex.works/job/fasterdev/
- fasterdev kibana: https://kibana.fasterdev.xrex.works/app/home#/
- exchange in fasterdev: https://magneto.fasterdev.xrex.works/advanced/BTC_USDT
- market pool jenkins build: https://jenkins.xrex.io/blue/organizations/jenkins/exchange-market-pool%2FBUILD/activity/

### Other
Service Desh: https://service-dash.xrex.works/

## 常用工具
### Redis Client
https://formulae.brew.sh/cask/another-redis-desktop-manager

## PyCharm 套件：
### ideavim
.ideavimrc
```
"" Source your .vimrc
"source ~/.vimrc

"" -- Suggested options --
" Show a few lines of context around the cursor. Note that this makes the
" text scroll if you mouse-click near the start or end of the window.
set scrolloff=5

" Do incremental searching.
set incsearch

" Don't use Ex mode, use Q for formatting.
map Q gq


"" -- Map IDE actions to IdeaVim -- https://jb.gg/abva4t
"" Map \r to the Reformat Code action
"map \r <Action>(ReformatCode)

"" Map <leader>d to start debug
"map <leader>d <Action>(Debug)

"" Map \b to toggle the breakpoint on the current line
"map \b <Action>(ToggleLineBreakpoint)

" basic
set hlsearch                    " highlight searches
set incsearch                   " do incremental searching, search as you type
set ignorecase                  " ignore case when searching
set smartcase                   " no ignorecase if Uppercase char present
set clipboard=unnamedplus  " 使用系统粘贴板(vim用y粘贴的内容也可以通过command + c 粘贴)

" 自動輸入中文
set keep-english-in-normal-and-restore-in-insert

" switch自動以英文為主
set keep-english-in-normal

nnoremap g; :action JumpToLastChange<CR>
imap <C-/> <ESC>:action HippieCompletion<CR>a
"imap <C-p> <ESC>:action HippieBackwardCompletion<CR>a

" jump to error
nnoremap gp :action GotoPreviousError<CR>

set relativenumber number
```


