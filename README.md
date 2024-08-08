`pip install mahdi_env`

`from mahdi_env import get_env()

`get_env()` returns all environment variables on a machine, [especially] including those inside `$HOME/.export` (if exists).

`get_env()` returns a special dictionary containing all environment variables as keys and their values as dictionary values. 
That kind of dict (I name it ENVDict does not throw an error when a key is not present; instead, it returns an empty string (''), allowing at least some part of the code to be runnable on another machine.

`get_env()` is the primary function of this package.

If `$HOME/.export` doesn't exist on that machine it just returns os.environ() that consists of all environment variables on that particular machine but in the form of that special dictype mentioned (ENVDict).

