# walter
Snakemake workflow for running multiple [methdemons](https://github.com/vesmanojlovic/methdemon/tree/master) in a cluster environment (or locally, but why...?).

# Set-up
To clone the repository, run
```
git clone https://github.com/vesmanojlovic/walter --recursive
cd walter
```
The `--recursive` flag is required to include the methdemon submodule.
Next, compile methdemon
```
cd resources/methdemon/
# edit the Makefile to contain your boost library path
make all
cd ../..
```
Finally, set up the virtual environment for the workflow
```
pyenv virtualenv 3.11 walter
pyenv activate walter
pip install -r requirements.txt
```

# Running walter
Example run
```
./walter.sh -c /users/user/scratch/config.yml -e slurm
```
For more details, execute `./walter.sh --help`.
