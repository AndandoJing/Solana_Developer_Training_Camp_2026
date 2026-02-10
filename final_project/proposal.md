项目名称

Solana Agent 任务悬赏托管平台（Bounty Escrow Agent）

💻 项目 Repo

TODO：填你的 GitHub repo 链接
（示例：https://github.com/your-username/solana-bounty-escrow-agent）

📌 项目简介

这是一个基于 Solana 的去中心化任务悬赏平台（Bounty）。发布者可以创建任务并将赏金锁定在链上托管账户中，领取者完成任务后提交交付，发布者确认后赏金会自动释放给领取者。

与传统平台不同，本项目引入了 Rule-based Agent：任何人都可以触发 check_and_execute()，但合约会根据任务状态与截止时间自动决定“放款 / 退款 / 不处理”。这让悬赏结算不依赖平台或人工介入，降低信任成本与纠纷处理成本。

🛠️ 技术栈

智能合约：Rust + Anchor Framework

前端：Next.js + TypeScript + Solana Wallet Adapter

工具：Solana CLI、Anchor CLI、@solana/web3.js

🎬 Demo 演示

🎥 视频演示：TODO（YouTube / Bilibili 链接）

🌐 在线 Demo（如有）：TODO（Vercel/Netlify 链接）

功能截图：TODO（可在此处贴 2–4 张关键流程截图：创建任务、锁定赏金、确认交付、自动退款/放款）

💡 核心功能

创建悬赏任务并锁定赏金：发布者创建任务，设置赏金金额、领取者地址（可选）、截止时间等参数，并将代币锁定在托管账户中。

提交交付 / 确认完成：领取者提交交付信息（可先做简单文本/链接字段），发布者确认后进入可放款状态。

Agent 自动结算（关键）：通过 check_and_execute()，合约根据链上时间与任务状态自动执行：

已确认 → 自动释放赏金给领取者

超过截止时间且未确认 → 自动退款给发布者

未满足条件 → 不处理

可追溯的链上状态：所有任务状态与结算结果记录在链上，便于公开验证与审计。

（可选加分）支持 SPL Token / USDC：赏金可使用 SPL Token（或 devnet USDC）。

✍️ 项目创作者

创作者昵称：TODO

联系方式：TODO（X / Telegram / Email 任意一种即可）

Solana 钱包地址（USDC）：TODO
