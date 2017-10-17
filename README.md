Ansible FFmpeg For Ubuntu, Debian or Mint
=========

A role to install ffmpeg 3.4 from source code. Based on official ffmpeg [Compilation guide for Ubuntu, Debian, or Mint](https://trac.ffmpeg.org/wiki/CompilationGuide/Ubuntu).

Allows to update and remove existed ffmpeg installation.


Role Variables
--------------

`defaults/main.yml`

| Name                | Default Value             | Description                         |
|---------------------|---------------------------|-------------------------------------|
| `ffmpeg_source_dir` | /usr/local/ffmpeg_sources | Sources path                        |
| `ffmpeg_build_dir`  | /usr/local/ffmpeg_build   | Build path                          |
| `ffmpeg_bin_dir`    | /usr/local/bin            | Binaries path                       |
| `ffmpeg_config`     | (see source)              | FFMPEG compilation config           |
| `ffmpeg_action`     | install                   | Install, uninstall or update ffmpeg |

Example Playbook
----------------

Install ffmpeg:

    - hosts: servers
      roles:
        - { role: "ffmpeg", tags: ["ffmpeg"] }

Update ffmepg:

    - hosts: servers
      roles:
        - { role: "ffmpeg", tags: ["ffmpeg"], ffmpeg_action: "update" }

License
-------

The gem is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).

Copyright (c) 2017 Sergey Zabolotnov
