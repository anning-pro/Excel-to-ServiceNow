日本語版：ユーザーガイドおよびExcel仕様書

1. オプション設定との整合性について

本ツールがExcelファイルを正しく解析するために、Excel内の見出しやシート名は、拡張機能の「設定（Options）」画面で定義されている内容と一致している必要があります。

シート名の指定: デフォルトでは「テーブル定義」および「選択肢リスト」という名前のシートを探します。シート名を変更した場合は、必ず設定画面の該当箇所も更新してください。

項目のマッピング: ツールは「カラム名」や「タイプ」といった見出し文字列を基準にデータを読み取ります。設計書のフォーマットに合わせて、設定画面でマッピング値を調整してください。

2. 「分類」列の使い方

「追加」: その行の定義を新しいフィールドとしてServiceNow上に作成します。

「修正」: 既存のフィールド定義を更新します。ラベルや最大長の変更などを一括で行う際に使用します。

空欄: 対象外として無視されます。

「追加」「修正」以外の値は不正値として扱い、Excelの行番号付きでエラー表示します。

3. 利用前のチェック項目

テーブル基本情報: シート上部にある「テーブルラベル」および「テーブル名」が正しく入力されているか確認してください。

フィールド型: String, Reference, Choice など、ServiceNowが対応している型を指定してください。詳細はテンプレート内の「CodeList」シートを参照してください。

参照先テーブル: 参照（Reference）型を選択した場合、参照先テーブルの物理名（例: incident, sys_user）が入力されているか確認してください。

English Version: User Guide & Excel Specifications

1. Consistency with Options settings

For this tool to parse Excel correctly, headers and sheet names in Excel must match the values defined in the Settings (Options) screen.

Sheet names: By default, the tool looks for sheets named "Table Definition" and "Choice List". If you rename them, update Settings as well.

Header mapping: The tool reads data based on header text (for example "Column name" or "Type"). Adjust mapping values to match your format.

2. How to use the Classification column

"add": Creates new fields in ServiceNow for those rows.

"edit": Updates existing field definitions (for example label or max length).

Blank: ignored (not processed).

Values other than add/edit are treated as invalid and shown as errors with Excel row numbers.

3. Pre-check items before upload

Table basic info: Ensure "Table label" and "Table name" in the upper section are correctly filled.

Field type: Use types supported by ServiceNow (String, Reference, Choice, etc.). See the "CodeList" sheet in the template.

Reference table: For Reference type, ensure the physical table name is provided (for example incident, sys_user).
