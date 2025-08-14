# Easywarp-MASQUE

An automatic Warp node switching tool (自动切换warp节点的工具) that uses the **MASQUE protocol** to connect to Warp with a single command (实现一行指令通过MASQUE协议连接warp).

## Usage (使用方法)

1.  **Install the Cloudflare WARP Client (安装Cloudflare WARP官方客户端):** Make sure you have the official Cloudflare WARP client installed on your system. You can get it from the [official website](https://1.1.1.1/).

2.  **Verify WARP Installation (验证WARP安装):** Open your command prompt or terminal and type `warp-cli status`. If a status message appears, you're good to go. (在控制台运行`warp-cli status`，若返回状态信息即可)

3.  **Start Easywarp-MASQUE (开始Easywarp-MASQUE):** Run the following command (assuming you have compiled `ezwarpm.cpp` to `ezwarpm.exe`):

    ```bash
    ezwarpm start
    ```
    *   **First Run (第一次运行):** The first time you run this, the script will scan for the best MASQUE nodes. Please be patient, as this process can take some time. (第一次运行会筛选节点，请耐心等待)

4.  **Check the Logs (查看运行情况):** To view the connection status and logs, use the following command:

    ```bash
    ezwarpm log
    ```

5.  **Stop Easywarp-MASQUE (停止Easywarp-MASQUE):** If you encounter errors or want to stop the script, use the following command:

    ```bash
    ezwarpm stop
    ```

6. **Update Warp Nodes (更新节点):** If you want to force a new scan for the best nodes, run the following command:
   ```bash
   ezwarpm update
   ```
   (若要更新节点池，运行`ezwarpm update`可以自动更新)

7. **Switch to Next Node (切换节点):** If you feel the current node is slow, this command will switch to the next best node in the list:
   ```bash
   ezwarpm next
   ```
   (如果觉得节点速度不佳，运行`ezwarpm next`可自动切换节点)

## About `warp.exe`

The included `warp.exe` is a third-party tool used for scanning Cloudflare IP addresses to find the fastest and most stable endpoints.
