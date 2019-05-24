Loadable libraries and perl binaries are mismatched
2019-05-24T00:03:00Z

While working on a Perl project, I have received an error message that I have never seen before. I did take a look at search engines, but no solutions there helped me. In the end I was able to figure out what's wrong, so I thought I should share it here.

    Util.c: loadable library and perl binaries are mismatched (got handshake key 0xc280000, needed 0xc180000)

This is more likely to happen if you are dealing with multiple versions of `perl` (note the word "mismatched"). For me though, that's usually not the case: I tend to download latest stable version via perlbrew and use it in all places.

Two solutions I could find online were:

- Clear `PERL5LIB` and `PERL_LOCAL_LIB_ROOT` environment variables
- Reboot your system

Neither worked for me. Those environment variables were already not set, and a reboot didn't help.

Turns out my issue was related to `carton`. See, very recently I reinstalled everything on my machine. And before doing so, I backed up my work folder to an external memory. Once my system was up again, I went to grab latest stable `perl` from perlbrew. Just before I did that a new version (5.30.0) was released. Do you see where it's going?

My backed up project included carton's locally installed modules folder: `local/`. But those modules were installed when latest stable version was 5.28.2, hence the "mismatch". Solution was to remove `local/`, and reinstall modules with `carton install`.
