## Setup
### For mac 
[install homebrew](https://brew.sh/)

Ensure homebrew is up-to-date, run:
1. `brew doctor`
2. `brew update`

Now that brew is up to date, run:

`brew install postgres`

### For windows
[Installer](https://www.postgresql.org/download/windows/)

### Run postgres
After installation open terminal and run `psql postgres`

If installed correctly, you should see output in your terminal similar to this: 

```bash
$ psql postgres
psql (11.2)
Type "help" for help.

$ postgres=# 
```