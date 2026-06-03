Stderr for source:  RMSD.md_working_7.dat   
Download: [zipped raw stdout](RMSD.md_working_7.dat.plumed.stdout.txt.zip) - [zipped raw stderr](RMSD.md_working_7.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: PDB2CONSTANT LABEL=rmsd_ref REFERENCE=reference.pdb
Maybe a missing space or a typo?
[runnervm3jyl0:49420] *** Process received signal ***
[runnervm3jyl0:49420] Signal: Aborted (6)
[runnervm3jyl0:49420] Signal code:  (-6)
[runnervm3jyl0:49420] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f98d8845330]
[runnervm3jyl0:49420] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f98d889eb2c]
[runnervm3jyl0:49420] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f98d884527e]
[runnervm3jyl0:49420] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f98d88288ff]
[runnervm3jyl0:49420] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f98d8ca5ff5]
[runnervm3jyl0:49420] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f98d8cbb0da]
[runnervm3jyl0:49420] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f98d8ca5a55]
[runnervm3jyl0:49420] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f98d8ca5a6f]
[runnervm3jyl0:49420] [ 8] plumed(+0x13209)[0x55dd39025209]
[runnervm3jyl0:49420] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f98d882a1ca]
[runnervm3jyl0:49420] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f98d882a28b]
[runnervm3jyl0:49420] [11] plumed(+0x134a5)[0x55dd390254a5]
[runnervm3jyl0:49420] *** End of error message ***
</pre>
{% endraw %}
