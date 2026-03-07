# ALICE-Collaboration

Real-time collaborative editing & version control platform

## License

AGPL-3.0

## Architecture

```
Frontend :3000  -->  API Gateway :8080  -->  Core Engine :8081
```

| Layer | Port | Technology |
|-------|------|-----------|
| Frontend | 3000 | Next.js 14, Tailwind CSS |
| API Gateway | 8080 | Rust, Axum |
| Core Engine | 8081 | Rust, Axum |

## ALICE Crate Integration

alice-presence, alice-sync, alice-vcs, alice-auth

## Endpoints

| Method | Path | Description |
|--------|------|-------------|
| `POST` | `/api/v1/sessions` | コラボレーションセッション作成 |
| `POST` | `/api/v1/sync` | リアルタイム同期（CRDT） |
| `POST` | `/api/v1/commit` | バージョンコミット |
| `GET ` | `/api/v1/history` | 変更履歴取得 |
| `GET ` | `/health` | ヘルスチェック |

## Quick Start

```bash
cd services/core-engine
cargo run --release
curl http://localhost:8081/health
```

## Author

Moroya Sakamoto
