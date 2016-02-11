To upgrade all packages installed via PIP you have to reinstall them. I found a command on Stack Overflow that does this neatly. 

    pip freeze --local | grep -v '^\-e' | cut -d = -f 1  | xargs -n1 pip install -U
