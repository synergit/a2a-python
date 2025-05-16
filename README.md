# A2A SDK (Prototype)

Early version of the A2A Python SDK.

## Virtual Env.

```bash
python3.13 -m venv .venv
source .venv/bin/activate
```

## Install SDK

```bash
pip install .
```

## Verify install

```py
import a2a
```

## Run Helloworld

Run Remote Agent

```bash
cd examples/helloworld
python __main__.py
# or 
uv run __main__.py
```

In another terminal, run the client

```bash
cd examples/helloworld
python test_client.py
# or 
uv run test_client.py
```

## License

This project is licensed under the terms of the [Apache 2.0 License](LICENSE).

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for contribution guidelines.
