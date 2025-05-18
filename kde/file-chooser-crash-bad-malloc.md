# Application crash with bad malloc when file chooser should be open 

After some upgrades an error began to popup every time I try to open or save a file.
It seems related to the qt file selector and didn't happen with gnome file chooser.

The console output is something like
```bash
terminate called after throwing an instance of 'std::bad_alloc'
  what():  std::bad_alloc
```

I found the solution here:
https://forum.manjaro.org/t/many-std-bad-alloc-errors-recently/149534

It seems the problem is the `.config/QtProject.conf` file.

## Solution

- Rename or remove `~/.config/QtProject.conf`


