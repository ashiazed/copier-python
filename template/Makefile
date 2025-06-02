.PHONY: bootstrap test lint typecheck format

bootstrap:
	@uvx pre-commit install
	@if [ ! -f uv.lock ]; then \
		echo "Creating uv.lock..."; \
		uv lock; \
	else \
		echo "uv.lock already exists. Skipping lock generation."; \
	fi

test:
	pytest -v

lint:
	ruff check src tests

format:
	ruff format src tests

typecheck:
	mypy src tests
