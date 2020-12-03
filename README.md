# GnosisLab Code Style Guide

## Git

Use LF line ending instead of CRLF or other file ending. While installing Git for Windows check-out `Checkout as-is, commit Unix-style` option. For linux user no additional setup is required.

## Python

Follow the PEP 8 Python style guide, except uses 2 spaces instead of 4. Please conform to the Google Python Style Guide, and use pylint to check your Python changes. Use the yapf auto-formatter to avoid arguing over formatting.

To install pylint, yapf and retrieve custom style definition:

```sh
pip install pylint yapf --user
wget -O .pylintrc https://raw.githubusercontent.com/GnosisLab/Coding_Guide/developement/pylintrc
wget -O .style.yapf https://raw.githubusercontent.com/GnosisLab/Coding_Guide/developement/style.yapf
```

## C/C++

Use clang-format to format your C/C++ code. To install on Ubuntu 16+, do:

```sh
sudo apt-get install -y clang-format
```

You can check the format of a C/C++ file with the following:

```sh
clang-format <my_cc_file> --style=google > /tmp/my_cc_file.cc
diff <my_cc_file> /tmp/my_cc_file.cc
```
