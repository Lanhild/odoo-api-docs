## Getting Started

To get your own local development copy of the documentation up and running follow these simple steps.

## Dependencies

#### Python 3

Python 3.x comes preinstalled on every major Linux distributions.

#### python3-pip

Install `python3-pip` using your distribution package manager.

## Development Context

All changes that you wish to bring to this documentation must be made through a pull request.

Thus, you will be using a feature branch to commit your changes.ch.

## Contributing a New Feature

1. Create your new feature branch

```bash
git branch feature/NewFeature
git checkout feature/NewFeature
```

2. Commit your changes to your branch

```bash
git commit -S -a -m "Add my amazing new feature"
```

3. Open a new pull request for approval and later merging

## Development cycle

To modify the documentation pages and preview your changes, see the following:

1. Create a new virtual environment

```bash
python -m venv venv
```

2. Source the virtual environment

```bash
source venv/bin/activate
```

3. Install dependencies

```bash
pip install mkdocs-material
```

4. Start the live server

```bash
mkdocs serve
```

5. Check if everything still runs in production mode

```bash
mkdocs build
```

6. [Commit your code](#contributing-a-new-feature)
