# psycopg2: Compiled

This repository stores the compiled version of psycopg2 for python environments
initialized with `virtualenv`. <mark>Reason</mark>: I compiled this once on my
Mac (which has an M1 chip) and got it to run. I have not been able to do it since.

## Conditions & Caveats

This will only work under a very narrow set of circumstances. If your project checks
all of these boxes, then you too can use this compiled version of psycopg2!

Another note: **DO NOT** use this for production.

Conditions:
1. You are using `psycopg2==2.9.3`, and need it to run in development, locally.
2. You are working on MacOS with an M1 (or later series) chip.

## Steps to start using psycopg2

Follow these steps to the letter, and it should work for you.

Steps:
1. Uninstall `psycopg2` and `psycopg2-binary` from your project. This includes removing `psycopg2` from any `requirements.txt` files.
2. Make sure you have `postgresql` installed on your computer. If not, give this a go (here)[https://formulae.brew.sh/formula/postgresql@14].
3. Delete any existing virtual environment(s) from your project.
4. At the root level of the project folder, create a new virtual environment with `virtualenv env`. *Yes, name your environment* `env`.
5. Clone this repository.
6. Drag the folders: `/psycopg2` and `/psycopg2-2.9.3.dist-info` into your environment at `/env/lib/python3.X/site-packages`.
7. Add `psycopg2==2.9.3` to your `requirements.txt` file.
8. You can now install your other dependencies with your `requirements.txt`.
9. Enjoy `psycopg2`.
