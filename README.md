<p  align="center">
<a  href="https://github.com/Egnod/koroviev">
<img width="500" src="https://gist.githubusercontent.com/Egnod/7cf16c66ed6da1656b069cf89b862aa8/raw/7bc095078d53f7384d5a5b44d47a2195fb76411c/krv_logo.svg">
</a>
<h1  align="center">
Koroviev
</h1>
</p>

## Install
```bash
pip3 install koroviev
```

## Help and init
For see commands list (man), type to console:
```bash
koroviev
```

For init, type to console (in project root folder):
```bash
koroviev init
```

## Create template example
Test project structure:
```bash
test_project
├── .koroviev_templates
├── .koroviev.toml
└── test_project
    └── cruds
```

For example, I add one template with name "crud" in my config file (.koroviev.toml) with two params
```toml
[setup]
language = 'python'
project_folder = 'test_project'
templates_folder = '.koroviev_templates'
template_extension = 'py'

[templates.crud]
comment = "my test template"
target_project_dir = "cruds/"
params = ["table", "segment"]
```

For easy get auto generate templates folder structure
```bash
koroviev structure generate
```
```bash
Create template type folder 'unary': '/home/user/projects/test_project/.koroviev_templates/unary'...
Create template file 'test': '/home/user/projects/test_project/.koroviev_templates/unary/test.py'...
```

Structure after template folder generate:
```bash
test_project
├── .koroviev_templates
│   └── unary
│       └── crud.py
├── .koroviev.toml
└── test_project
    └── cruds
```


