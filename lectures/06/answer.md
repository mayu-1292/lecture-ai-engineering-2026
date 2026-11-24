# 第6回 解答

## 演習

<!-- [tool call] の行は、表示された行をそのまま貼り付けてください。終わらなかった STEP は、空欄のままでかまいません。 -->

- STEP 1 のツールの名前：glossary_search_glossary
- STEP 2 の [tool call]：glossary_search_glossary({'query': '3レベル'})
- STEP 3 の [tool call]：fetch_fetch({'url': 'https://modelcontextprotocol.io/'})
- STEP 4 の [tool call]：aws_aws___search_documentation({'search_phrase': 'What is S3 Versioning', 'topics': ['general']})
- 気づき・疑問：

## 宿題

<!-- 基礎・実装・発展のどれか1つに取り組めば完了です。 -->

- 取り組んだレベル：基礎
- やったこと：app/mcp_server.py に server.tool()(tools.get_lecture_summary) を追加し、ツール一覧やトレース、pytest（21 passed）で動作確認した。
- 結果：`--list-tools` で `glossary_get_lecture_summary` が一覧に追加されたことを確認し、`uv run pytest -q` で全21件のテストが通過した（`21 passed`）。[cite: 9, 14]（「第2回では何を学びますか？」のトレース実行も確認）
- 気づき・疑問：エージェント側のコードや mcp_servers.json を変えずにサーバー側の公開ツールを増やせた。--trace 実行時は一時的な 503 エラーが出たため時間を置いて再確認した。
