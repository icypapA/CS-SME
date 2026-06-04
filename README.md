CS Match Brain
Local, repo-aware durable memory for Counter-Strike match analysis and strategy.
CS Match Brain exposes a local memory layer through MCP. It stores match history, player stats, and map strategies in SQLite with FTS5 search, runs fully on your machine, and makes no cloud calls.

Install
CS2 Plugin
macOS or Linux:
bashbash -c "$(curl -fsSL https://raw.githubusercontent.com/yourname/cs-match-brain/HEAD/install.sh)"
Then restart your CS2 server or reload the plugin.
Verify:
bashcs2 mcp get cs-match-brain
You should see enabled: true.
CSGO Legacy
macOS or Linux:
bashbash -c "$(curl -fsSL https://raw.githubusercontent.com/yourname/cs-match-brain/HEAD/csgo/install.sh)"
Then restart the server session.
Verify:
bashcsgo mcp get cs-match-brain

Usage
bash# บันทึก match ล่าสุด
cs-match-brain log --map de_dust2 --score 16-12

# ค้นหา strategy ที่เคยบันทึกไว้
cs-match-brain search "B site execute"

# ดู player stats สะสม
cs-match-brain stats --player "yoursteamid"
