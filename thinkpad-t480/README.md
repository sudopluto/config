# thinkpad t480 config
config for the first computer I bought with my own money

---
- operating system
    - Fedora 30
    - default theme for most applications

- bios settings
    - enable thunderbolt assist

- power
    - use tlp
    - investigate thermal throttling & possible solution
        - f31: dptfxtract 1.4.1, thermald 1.9, and kernel 5.3
            - https://github.com/intel/dptfxtract/issues/6
        - lenovo firmware update?
            - https://forums.lenovo.com/t5/Other-Linux-Discussions/X1C6-T480s-low-cTDP-and-trip-temperature-in-Linux/m-p/4513821#M13563
