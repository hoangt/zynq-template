# Template design for ZYNQ and ZYNQ Ultrascale+ ZC702 and ZC706

This project is a collection of scripts to automate the generation of the
necessary files to boot a minimal image of Linux on the Xilinx ZYNQ-based
development boards.

By editing the script for `scripts/vivado.tcl`, users can instantiate their own
IP blocks on the programming logic. The device tree will be updated
automatically.

The root file system has been generated with the template projects from
Petalinux. Users can replace or customize the content of `out/<BOARD>/root` to
add more features.

Scripts are tested with Vivado 2018.2.

## Supported Development Boards

  - Zynq ZC702 and ZC706
  - Zynq Ultrascale+ ZCU102


## Usage

```
$ [ETHADDR=<xx:xx:xx:xx:xx:xx>] [BOARD=<zc702|zc706|zcu102>] make
```

All configuration files, temporary built objects and boot images will be
generated in `out/<BOARD>`.  This includes the files to copy onto SD
card to boot on hardware. Please refer to [Xilinx Wiki](https://xilinx-wiki.atlassian.net/wiki/spaces/A/pages/18842385/How+to+format+SD+card+for+SD+boot)
to partition and format the SD card appropriately.
