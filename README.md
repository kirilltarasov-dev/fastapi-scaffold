# ⚡ fastapi-scaffold

A modern, opinionated project scaffolder for FastAPI 🦄. Easily generate production-ready boilerplate code for your next backend project with support for:

- Docker & docker-compose
- Makefile & `.env` files
- SQLAlchemy & JWT Auth
- CI/CD (GitHub Actions)
- Ruff, Black, Pre-commit
- Pyproject-based dependency management via [uv](https://github.com/astral-sh/uv)

---

## 🧰 Features

| Feature            | Description                                    |
| ------------------ | ---------------------------------------------- |
| `--with-db`        | Adds SQLAlchemy base, session, and user model  |
| `--with-auth`      | Adds JWT-based authentication + OAuth2 handler |
| `--with-ci`        | GitHub Actions CI workflow for lint/test       |
| `--with-precommit` | Pre-commit config with Ruff and Black          |
| `pyproject.toml`   | uv-based dependency management                 |
| `Dockerfile(.dev)` | Lightweight build and dev environment          |
| `Makefile`         | Helpful run/lint/test targets                  |

---

## 🚀 Quick Start

```bash
python3 fastapi-init.py myapp \
  --with-db \
  --with-auth \
  --with-ci \
  --with-precommit
```

Then:

```bash
cd myapp
uv venv .venv
source .venv/bin/activate
make install
make run
```

---

## 📁 Generated Project Structure

```
myapp/
├── .env.example
├── .gitignore
├── Dockerfile
├── Dockerfile.dev
├── docker-compose.yml
├── Makefile
├── pyproject.toml
├── uv.lock
├── app/
│   ├── main.py
│   ├── db/                  # if --with-db
│   └── auth/                # if --with-auth
├── tests/
├── .github/workflows/ci.yml     # if --with-ci
├── .pre-commit-config.yaml      # if --with-precommit
├── .ruff.toml                   # if --with-precommit
└── README.md
```

---

## 🧪 Example: All Options

```bash
python3 fastapi-init.py my-secure-app \
  --with-db \
  --with-auth \
  --with-ci \
  --with-precommit
```

---

## 💡 Requirements

- Python ≥ 3.11
- [uv](https://github.com/astral-sh/uv): `pip install uv`
- Git
- Docker (for container workflows)

---

## 📦 Installation

No installation required — just run the script:

```bash
python3 fastapi-init.py <your_project_name> [flags]
```

For frequent use, install via `pipx` or alias the script:

```bash
alias fastapi-init="python3 /path/to/fastapi-init.py"
```

---

## 🧱 Roadmap

- [ ] Support for `--with-migrations` (Alembic)
- [ ] PostgreSQL support (`--with-postgres`)
- [ ] Template support for REST API modules
- [ ] CLI packaging as `fastapi-init` via `setuptools`

---

## 🛡 License

MIT License. Use freely, modify generously, and build awesome backends!

---

## 👩‍💻 Author

Crafted with ❤️ by Kirill Tarasov.

Pull requests and improvements welcome!
