# Claude Code スラッシュコマンド一覧

2026年11月時点でまとめた Claude Code のスラッシュコマンド一覧。
`/` を入力するとセッション内で使えるコマンドが出て、続けて文字を打つと絞り込める。
プラン・プラットフォーム・環境によって表示されないコマンドもある。

## 組み込みコマンド

| コマンド | 別名 | 説明 |
|---|---|---|
| `/add-dir <path>` | | 作業ディレクトリを追加 |
| `/advisor [model\|off]` | | 要所で別モデルに相談する Advisor のオン/オフ |
| `/agents` | | サブエージェントの管理 |
| `/artifacts` | | 自分/共有のアーティファクトを一覧してセッションに添付 |
| `/auto-mode-setup` | | プロジェクトと最近のセッションから `autoMode.environment` の設定案を作る |
| `/autocompact [auto\|tokens]` | | 自動コンパクトが走るコンテキスト量を設定 |
| `/autofix-pr [prompt]` | | PRを監視してCIやレビュー指摘の修正をpushするWebセッションを開始 |
| `/background [prompt]` | `/bg` | セッションをバックグラウンドエージェントとして切り離す |
| `/branch [name]` | | 会話のブランチを作って切り替え |
| `/btw [question]` | | 会話コンテキストに残さずに横道の質問をする |
| `/bug [report]` | `/share` | バグ報告・セッション共有（同意あり） |
| `/cd <path>` | | 会話を保ったまま作業ディレクトリを変更 |
| `/chrome` | | Claude in Chrome の設定 |
| `/clear [name]` | `/reset`, `/new` | コンテキストなしで新しい会話を開始 |
| `/color [color\|default]` | | プロンプトバーの色を設定 |
| `/compact [instructions]` | | 会話を要約してコンテキストを空ける |
| `/config [key=value ...]` | `/settings` | 設定を開く・直接変更 |
| `/context [all]` | | コンテキストの中身を可視化し、改善案を表示 |
| `/copy [N]` | | 最新（またはN個前）の応答をクリップボードにコピー |
| `/cost` | | `/usage` の別名 |
| `/design consent` / `/design revoke` | | Claude Design へのアクセス許可/取り消し |
| `/design-login` | | `/design-sync` 用に Claude Design を認可 |
| `/desktop` | `/app` | デスクトップアプリでセッションを続ける |
| `/diff` | | 対話型の差分ビューアを開く |
| `/effort [level\|auto\|status\|ultracode]` | | 推論の深さ（effort）を設定 |
| `/exit` | `/quit` | 終了（またはアタッチ中のバックグラウンドセッションから離脱） |
| `/export [filename]` | | 会話をテキストで書き出す |
| `/extra-usage` | | レート制限時に使い続けるための追加利用を設定 |
| `/fast [on\|off]` | | Fastモードの切り替え（対応アカウントのみ） |
| `/feedback [report]` | | `/bug` と同じダイアログ |
| `/focus` | | フルスクリーン表示で簡易フォーカスビューに切り替え |
| `/fork [prompt]` | | 会話を新しいバックグラウンドセッションに複製 |
| `/goal [condition\|clear]` | | ターンをまたいで追い続けるゴールを設定 |
| `/heapdump` | | メモリ診断を書き出す（隠しコマンド・機密情報を含む可能性あり） |
| `/help` | | ヘルプと使えるコマンドを表示 |
| `/hooks` | | フック設定を表示 |
| `/ide` | | IDE連携の管理 |
| `/import [codex\|gemini\|cursor]` | | 他ツールのルール・MCP・スキルを取り込む |
| `/init` | | CLAUDE.md にプロジェクトガイドを作成 |
| `/insights` | | ローカルセッションと利用傾向のHTMLレポートを生成 |
| `/install-github-app` | | リポジトリに Claude GitHub App をセットアップ |
| `/install-slack-app` | | Claude Slack アプリをインストール |
| `/keybindings` | | キーバインド設定ファイルを開く |
| `/list-agents` | `/peers` | 到達可能なサブエージェント・チームメイト・セッションを一覧 |
| `/login` | | Anthropic にサインイン |
| `/logout` | | サインアウト |
| `/mcp [reconnect\|enable\|disable]` | | MCP接続とOAuthの管理 |
| `/memory` | | CLAUDE.md と自動メモリを編集 |
| `/mobile` | `/ios`, `/android` | モバイルアプリのQRコードを表示 |
| `/model [model]` | | モデル切り替え（新規セッションにも保存） |
| `/output-style [style]` | | 出力スタイルの一覧・切り替え |
| `/passes` | | 対象アカウントなら無料の Claude Code 1週間を共有 |
| `/permissions` | `/allowed-tools` | ツールの許可/確認/拒否ルールを管理 |
| `/plan [description]` | | プランモードに入る |
| `/plugin [subcommand]` | | プラグインの一覧・インストール・有効化/無効化 |
| `/powerup` | | 機能紹介のミニレッスン |
| `/pr-comments [PR]` | | GitHub PR のコメントを取得して表示 |
| `/privacy-settings` | | プライバシー設定（Pro/Max） |
| `/radio` | | Claude FM をブラウザで開く（地域限定） |
| `/rate-limit-options` | | 利用上限に達したときの選択肢を表示 |
| `/recap` | | セッションを一文で要約 |
| `/release-notes` | | リリースノートを表示 |
| `/reload-plugins [--force]` | | プラグインを再読み込みしMCPの変更を反映 |
| `/reload-skills` | | 再起動なしでスキル/コマンドを再読み込み |
| `/remote-control` | `/rc` | ローカルセッションを claude.ai やアプリから操作可能にする |
| `/remote-env` | | クラウドエージェントの既定環境を選ぶ |
| `/rename [name]` | | セッション名を変更 |
| `/restart` | `/update` | 再起動してアップデートを適用し、セッション再開 |
| `/resume [session]` | `/continue` | IDか名前で会話を再開 |
| `/review` | | `/code-review` の別名 |
| `/rewind` | `/checkpoint`, `/undo` | コード/会話をチェックポイントに戻す |
| `/sandbox` | | サンドボックスモードの切り替え |
| `/schedule [description]` | `/routines` | クラウドのルーティン（定期実行）の作成・更新・実行 |
| `/scroll-speed` | | フルスクリーン表示のスクロール速度 |
| `/security-review` | | ブランチの差分をセキュリティ観点でチェック |
| `/setup-bedrock` | | Amazon Bedrock の認証・リージョン・モデル設定 |
| `/setup-vertex` | | Google Cloud の設定 |
| `/skills` | | スキル一覧と表示管理 |
| `/stats` | | `/usage` の Stats タブを開く |
| `/status` | | バージョン・モデル・アカウント・接続状態を表示 |
| `/statusline` | | ステータスラインを設定 |
| `/stickers` | | ステッカーを注文 |
| `/stop` | | アタッチ中のバックグラウンドセッションを停止 |
| `/subtask <task>` | | 結果が会話に戻るバックグラウンドのサブエージェントを開始 |
| `/tasks` | `/bashes` | バックグラウンド作業の表示・管理 |
| `/team-onboarding` | | 利用履歴からチーム向けオンボーディング資料を作成 |
| `/teleport` | `/tp` | クラウドセッションをターミナルに持ってくる |
| `/terminal-setup` | | Shift+Enter などターミナル用キー設定 |
| `/theme` | | テーマ切り替え |
| `/tui [default\|fullscreen]` | | 描画方式の切り替え |
| `/ultrareview [PR\|branch]` | | クラウド版 `/code-review ultra` を実行 |
| `/upgrade` | | 上位プランへのアップグレードページを開く |
| `/usage` | | コスト・プラン上限・利用統計 |
| `/usage-credits` | | 利用クレジットの設定・管理者への申請 |
| `/voice [hold\|tap\|off]` | | 音声入力（Claude.ai アカウント） |
| `/web-setup` | | ローカルのGitHub認証情報を Web版 Claude Code に接続 |
| `/workflows` | | 実行中・完了したワークフローの進捗 |

## バンドル済みスキル（コマンドとして呼べる）

| コマンド | 別名 | 説明 |
|---|---|---|
| `/artifact-capabilities` | | アーティファクトの実行時機能リファレンスを読み込む |
| `/artifact-diagramming` | | アーティファクト内の図のガイドを読み込む |
| `/batch <prompt>` | | 大きな変更をworktreeに分割し、それぞれバックグラウンドで処理 |
| `/claude-api [subcommand]` | | Claude API / Managed Agents のリファレンスを読み込む |
| `/claude-in-chrome [task]` | | Claude in Chrome でブラウザ作業 |
| `/code-review [options] [target]` | | 差分・PR・ブランチ・パスをレビューし、修正も可能 |
| `/dataviz [request]` | | グラフ・ダッシュボードのデザイン支援 |
| `/debug [description]` | | デバッグログを有効化してセッションログを解析 |
| `/design [brief]` | | Claude Design でUIデザインを作成 |
| `/design-sync [prompt]` | | ReactのデザインシステムをClaude Designに同期 |
| `/doctor [prompt-audit [path]]` | `/checkup` | インストールと設定を診断し、改善案を出す |
| `/fewer-permission-prompts` | | よく使う読み取り系ツールの許可リスト案を出す |
| `/loop [interval] [prompt]` | `/proactive` | セッション中、プロンプトを繰り返し実行 |
| `/plugin-authoring` | | プラグイン開発のリファレンスを読み込む |
| `/run` | | アプリを起動・操作して変更を観察 |
| `/run-skill-generator` | | `/run` と `/verify` 用のプロジェクト固有の土台を作る |
| `/simplify [target]` | | 変更コードを再利用・簡素化・効率の観点で見直す |
| `/skill-doctor` | | スキルのコンテキスト消費と使用状況を表示 |
| `/slides [brief]` | | Claude Slides でプレゼンを作成 |
| `/update-config [request]` | | 自然言語で `settings.json` を変更 |
| `/verify` | | ビルド・起動・テストでコード変更を確認 |
| `/workflow-authoring` | | ワークフロー作成のリファレンスを読み込む |
| `/deep-research <question>` | | Web調査してソース付きレポートを返す（ワークフロー） |

## その他の入力

| 入力 | 説明 |
|---|---|
| `!コマンド` | Bashモード：シェルコマンドを実行して出力を会話に追加 |
| `@パス` | ファイルを指定してコンテキストに追加 |
| `/mcp__<サーバー>__<プロンプト>` | 接続中のMCPサーバーが公開するプロンプト |
| `.claude/commands/*.md`, `.claude/skills/` | 自作のカスタムコマンド/スキル（`~/.claude/` に置くと全プロジェクト共通） |

---

出典: [gradually.ai – Claude Code Commands](https://gradually.ai/en/claude-code-commands), [Arantic Docs – Slash Commands & Shortcuts](https://arantic-docs.pages.dev/claude-code/commands), [公式ドキュメント](https://code.claude.com/docs/en/interactive-mode)
バージョンによって増減するので、最新は Claude Code で `/help` を確認。
