Stderr for source:  plumed_ex1.dat   
Download: [zipped raw stdout](plumed_ex1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_ex1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action METAD with label metad : action cv has no component named cv (hint! the components in this actions are: cv.x cv.y cv.z )
[fv-az1778-96:05539] *** Process received signal ***
[fv-az1778-96:05539] Signal: Aborted (6)
[fv-az1778-96:05539] Signal code:  (-6)
[fv-az1778-96:05539] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f6df9042520]
[fv-az1778-96:05539] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f6df90969fc]
[fv-az1778-96:05539] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f6df9042476]
[fv-az1778-96:05539] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f6df90287f3]
[fv-az1778-96:05539] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f6df94a2b9e]
[fv-az1778-96:05539] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f6df94ae20c]
[fv-az1778-96:05539] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f6df94ae277]
[fv-az1778-96:05539] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f6df94ae52b]
[fv-az1778-96:05539] [ 8] plumed(+0x12f48)[0x55ea1a094f48]
[fv-az1778-96:05539] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f6df9029d90]
[fv-az1778-96:05539] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f6df9029e40]
[fv-az1778-96:05539] [11] plumed(+0x131e5)[0x55ea1a0951e5]
[fv-az1778-96:05539] *** End of error message ***
</pre>
{% endraw %}
