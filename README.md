# scx_replaced
本リポジトリは，[ComSys2026](https://sigos.ipsj.or.jp/event/comsys2026/) の発表論文「特定用途スケジューラの sched_ext による置き換え可能性の検証」で使用したスケジューラの実装を公開するものである．

本リポジトリでは，以下2つのスケジューラを公開している．
1. `scx_replaced`
    - 論文 [In Serverless, OS Scheduler Choice Costs Money: A Hybrid Scheduling Approach for Cheaper FaaS](https://dl.acm.org/doi/10.1145/3652892.3700757) で提案されたハイブリッドスケジューラを，ghOSt による実装から sched_ext による実装に置き換えたスケジューラ．
    - FIFO/CFS のハイブリッドスケジューリングを行う．具体的には，各タスクをまず FIFO でプリエンプションなしに実行する．その後，FIFO 実行で終了しなかったタスクのみを CFS に移行して実行する．
2. `scx_extended`
    - `scx_replaced` を拡張したスケジューラ．
    - タスクの初回実行時のみ，ランダムな CPU で短時間の割込実行を行い，その後，FIFO/CFS のスケジューリングに移行する．

## Requirements
TBA

## Build and Install
TBA

## Usage
TBA
