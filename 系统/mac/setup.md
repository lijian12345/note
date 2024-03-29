## 新mac设置

### 系统


- sys perf

  - Accessibility

    - Pointer Control - Trackpad Options - Enable dragging - 3 finger drag(三指拖移)

  - Trackpad

    - Point & Click - Tap to click(勾选轻触点击)
    - Scroll & Zoom - 取消勾选Scroll direction: Natural（跟scroll-reverser配合用）
    - More Gestures - swipe between pages(取消勾选)

  - Keyboard

    - Text

      - 取消勾选Correct spelling automatically

    - Shortcuts

      - Input Sources: 取消勾选Select the previous input source和Select next source in Input menu，用搜狗输入法就够了

      - Mission Control: Show Desktop(取消勾选f11显示桌面)

      - App Shortcuts:

        - typora:

        ```
        Code Fences: shift+cmd+k
        Ordered List: cmd+/
        Unordered List: cmd+.
        Source Code Mode: cmd+~
        ```

      - Function Keys: 添加vscode，chrome，idea

    - Input Sources：删除多余的输入法，只保留搜狗输入法

  - Dock & Menu Bar: 设置位置在右边并调整大小

  - Mission Control - Hot Corners: 右上角设置为桌面，双屏使用需对齐右侧边界

- 其他设置

  
  - 输入法问题：

      - 开启英文输入法长按连续输入，需要重启（参考https://zihengcat.github.io/2018/08/02/simple-ways-to-set-macos-consecutive-input/）：
  
        ```
        defaults write -g ApplePressAndHoldEnabled -bool false
        ```
  
      - keyboardholder可以为不同的应用固定输入法：
  
        ```
        bi keyboardholder
        ```
  
  - trash添加data added一列表示删除日期
  
  
  - 使用touch id代替命令行输入密码：https://dev.to/equiman/how-to-use-macos-s-touch-id-on-terminal-5fhg
  
    - ```
      code /etc/pam.d/sudo
      auth sufficient pam_tid.so
      ```

## 软件安装与设置

- 以下为不建议使用brew的软件：

  - 搜狗输入法

  - Logitech options+

  - idea

- app store里安装的软件：

  - iRightMouse（付费。。。说实话功能有点少）
  - Text Scanner（ocr)

- .zshrc配置

  - ```
    # brew alias
    alias b='brew'
    alias bi='brew install'
    alias bui='brew uninstall'
    alias bs='brew search'
    alias bl='brew list'
    ```

- 使用brew安装的软件：

  - ```
    bi --cask 1password
    ```

  - ```
    bi --cask scroll-reverser
    ```

    - Scrolling Axes：勾选Reverse Vertical和Reverse Horizontal
    - Scrolling Devices：勾选Reverse Trackpad
    - start at login

  - ```
    bi --cask typora
    ```

  - ```
    bi --cask clipy
    ```

    - 多重剪贴板，可以导入导出

  - ```
    bi --cask macgesture
    ```

    - 鼠标手势(触摸板也可以识别)，下为导入导出语句

      ```
      defaults import com.codefalling.MacGesture backup.list
      defaults export com.codefalling.MacGesture backup.plist
      ```

    - 手势示例：[backup](resources/backup.plist)

  - ```
    bi deepl
    ```

  - ```
    bi --cask xnviewmp
    ```

    - Tools > Settings > General -- General tab -- Mode when starting with a file -- Normal.

  - ```
    bi --cask tiles
    ```

  - ```
    bi --cask hiddenbar
    ```

    - sudo xattr -r -d com.apple.quarantine /Applications/Hidden\ Bar.app
    - 取消勾选show prefrences on launch

  - ```
    bi java11
    ```

    - sudo ln -sfn /usr/local/opt/openjdk@11/libexec/openjdk.jdk /Library/Java/JavaVirtualMachines/openjdk-11.jdk

  - ```
    bi git
    ```

  - ```
    bi libpq
    ```

    - 用于pg_dump，位置在/usr/local/opt/libpq/bin下面

  - ```
    bi --cask iterm2
    ```

    - Mac自带zsh，安装powerlevel10k

    - Font size: 15，window: 100*25，光标：竖线

  - ```
    bi --cask docker
    ```

    - Enable k8s

  - ```
    bi --cask visual-studio-code
    ```

    - 开启同步

  - ```
    bi --cask redisinsight
    ```

  - ```
    bi wget
    ```

  - 解压缩：

    ```
    bi keka
    ```


- 暂时未用

  - bi --cask popclip

  - bi --cask bettertouchtool

​	