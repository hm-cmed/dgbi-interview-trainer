# DGBI 面接トレーナー（自己採点版） / Brain–Gut Communication Self-Trainer

脳腸相関障害（DGBI）の患者との対話を、台本と自己採点で練習するオフライン教材です。一般医・プライマリケア医が Rome V "Level 1 psychosocial care" のコミュニケーション技能を、AI を使わずに自習できます。

An offline, self-scored trainer for physician–patient communication in disorders of gut–brain interaction (DGBI). No API, no server, no data leaves the browser. The AI-dialogue version runs separately on Google AI Studio.

## 特徴 / Features

- **完全オフライン**：単一の `index.html` のみ。API キー不要、サーバー不要、通信なし。
- **5 ケース（C1–C5）**：不信の IBS 初診、FD の脳腸相関説明、神経修飾薬の stigma、難治重複例の紹介判断、明確な診断を好む高齢患者。
- **4 原則の自己採点**：能動的傾聴・関心事の引き出し・非難しない説明／陽性的診断・自己効力感の促進を自己チェック。
- **MILESTONE 判定**：チェックに応じて信頼度（trust）が動き、Lv1–5 の到達段階と「次に伸ばす一手」を表示。
- **進捗保存**：結果はブラウザの `localStorage` に保存（端末内のみ）。

## 使い方 / Usage

各ケースで患者の発話を読み、**模範解答を見る前に自分ならどう返すかを声に出してから**、実際に満たせた行動をチェックして「採点する」を押します。

## 公開 / Deploy on GitHub Pages

このリポジトリを push し、GitHub の **Settings → Pages → Build and deployment → Source** を **GitHub Actions** に設定すると、`main` への push で自動公開されます。数十秒後に `https://<ユーザー名>.github.io/<リポジトリ名>/` で閲覧できます。

Actions を使わない場合は、Source を **Deploy from a branch → main / (root)** にしても公開できます（`.nojekyll` を含めているため Jekyll 処理はスキップされます）。

## ライセンス / License

MIT License（`LICENSE` 参照）。教材内容は Rome V および関連エビデンス（Drossman 2021、Kaptchuk 2008/2010、Yan 2015、Basnayake 2022、Ko 2024 ほか）に基づく教育目的の再構成です。

## 位置づけ / Context

DGBI 精神療法オンデマンド訓練プログラム（MIND モデル準拠）の第二層・第三層を、AI なしで再現したオフライン自己採点版です。AI 模擬患者との動的対話・自動フィードバックは Google AI Studio 版で提供されます。

Sapporo Medical University — Center for Medical Education
