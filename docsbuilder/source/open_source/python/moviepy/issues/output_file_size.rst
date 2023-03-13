=======================
Output file size
=======================

.. |br| raw:: html

   <br>

.. csv-table::
   :header: No.,Title,Status
   
   1,`write_gif() output file size is large #811 <https://github.com/Zulko/moviepy/issues/811>`_,``closed``

|

____ 

|

1. write_gif() output file size is large #811
=============================================

▶︎ Solution 1
-------------

Using ffmpeg instead of imageio can significantly reduce the file size |br|
For a seven second gif I got the following results. （`Solution 1 link <https://github.com/Zulko/moviepy/issues/811#issuecomment-564953684>`_）

ffmpeg : ``19MB`` |br|
imageio : ``39MB``

.. code-block::
   
   [ ] gif_clip.write_gif('gif_clip_imageio.gif',fps=25,program= 'imageio')
   [✓] gif_clip.write_gif('gif_clip.gif',fps=25,program= 'ffmpeg')

|

____ 

|

▶︎ Solution 2
-------------

resize （`Solution 2 link <https://github.com/Zulko/moviepy/issues/811#issuecomment-1001984653>`_）

.. code-block::
   
   clip = VideoFileClip("input.mp4").subclip('2:09:05', '2:09:17').resize(0.5)

____ 

|
|
|



.. toctree::
   :maxdepth: 3

