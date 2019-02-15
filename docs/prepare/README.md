# 前言

gitbook 需要使用 `node.js` 命令

因此，在具体使用之前需要在机器上安装 `node.js`，如果机器中之前已经安装过 `node.js`，这里可以直接跳过。

- **node 官网：** https://nodejs.org/

- **nvm github：** https://github.com/coreybutler/nvm-windows/releases

- **阿里 `cnpm` 镜像：** http://npm.taobao.org/

# node 官网资源下载

node 官网 LTS 资源下载链接（以下下载链接中 node 版本为 `v10.15.1`，其中包含 `v6.4.1` npm）：

<table class="download-matrix full-width" style="text-align: center;">
  <tbody>
    <tr>
      <th style="text-align: center;">Windows 安装程序 (.msi) (.msi)</th>
      <td colspan="3"><a href="https://nodejs.org/dist/v10.15.1/node-v10.15.1-x86.msi">32-bit</a></td>
      <td colspan="3"><a href="https://nodejs.org/dist/v10.15.1/node-v10.15.1-x64.msi">64-bit</a></td>
    </tr> 
    <tr>
       <th style="text-align: center;">Windows 二进制包 (.zip)</th>
       <td colspan="3"><a href="https://nodejs.org/dist/v10.15.1/node-v10.15.1-win-x86.zip">32-bit</a></td>
       <td colspan="3"><a href="https://nodejs.org/dist/v10.15.1/node-v10.15.1-win-x64.zip">64-bit</a></td>
    </tr>
    <tr>
       <th style="text-align: center;">macOS 安装程序 (.pkg)</th>
       <td colspan="6"><a href="https://nodejs.org/dist/v10.15.1/node-v10.15.1.pkg">64-bit</a></td>
    </tr>
    <tr>
       <th style="text-align: center;">macOS 二进制包 (.tar.gz)</th>
       <td colspan="6"><a href="https://nodejs.org/dist/v10.15.1/node-v10.15.1-darwin-x64.tar.gz">64-bit</a></td>
    </tr>
    <tr>
       <th style="text-align: center;">Linux 二进制包 (x64)</th>
       <td colspan="6"><a href="https://nodejs.org/dist/v10.15.1/node-v10.15.1-linux-x64.tar.xz">64-bit</a></td>
    </tr>
    <tr>
       <th style="text-align: center;">Linux 二进制包 (ARM)</th>
       <td colspan="2"><a href="https://nodejs.org/dist/v10.15.1/node-v10.15.1-linux-armv6l.tar.xz">ARMv6</a></td>
       <td colspan="2"><a href="https://nodejs.org/dist/v10.15.1/node-v10.15.1-linux-armv7l.tar.xz">ARMv7</a></td>
       <td colspan="2"><a href="https://nodejs.org/dist/v10.15.1/node-v10.15.1-linux-arm64.tar.xz">ARMv8</a></td>
    </tr>
    <tr>
       <th style="text-align: center;">源码</th>
       <td colspan="6">
         <a href="https://nodejs.org/dist/v10.15.1/node-v10.15.1.tar.gz">node-v10.15.1.tar.gz</a>
       </td>
    </tr>
  </tbody>
</table>

# github NVM 下载

github 中 nvm 只包含 windows 版本，mac 与 linux 平台无法使用。

![github-nvm-win](./_images/github-nvm-win.png)