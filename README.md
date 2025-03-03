# wang-ruifan的个人主页

## 本地部署指南

1. 启用WSL2  
    启用CPU虚拟化  
    设置中搜索开发者设置并打开  
    在控制面板-程序和功能-启用或关闭Windows功能中启用“适用于Linux的Windows子系统”，点击确定，完成后重启  
    打开PowerShell并输入`wsl --set-default-version 2`，设置WSL2为默认版本  
2. 安装Ubuntu 20.04  
    在Microsoft Store中搜索Ubuntu 20.04并安装  
     安装完成后打开Ubuntu 20.04，设置用户名和密码
3. 安装ruby
    在vscode或终端中打开Ubuntu 20.04  
    输入下列命令安装ruby  、

    ```bash
    sudo apt update
    sudo apt install ruby-full build-essential zlib1g-dev
    ```

    为gem添加用户的路径配置

    ```bash
    echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
    echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
    echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
    source ~/.bashrc
    ```

4. 安装Jekyll  
    输入下列命令安装Jekyll

    ```bash
    gem install jekyll bundler
    ```

5. 进入项目文件夹并编译  
    在vscode或终端中打开项目文件夹  
    安装bundler组件  

    ```bash
    bundler install
    ```

    编译

    ```bash
    bundle exec jekyll serve
    ```

    等待一会，当终端中出现

    ```bash
    Server address: http://127.0.0.1:4000/
    Server running... press ctrl-c to stop.
    ```

    时，打开浏览器并输入`http://127.0.0.1:4000/`即可查看网页