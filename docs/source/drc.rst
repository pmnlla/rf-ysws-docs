Passing DRC
===========

KiCAD has a built in function to ensure your PCB can be manufactured without bridges, missing connections, or other manufacturing issues.

However, this function often fails to reflect the manufacturing capabilities of modern fabricators **by default**. Thereby, even a known good PCB can fail to pass.

Where to find DRC?
------------------

In an instance of KiCAD's PCB editor, with a design open, head into Tools, then Design Rules Check.

.. image:: img\kicad_xOUEhjUNW0.png
   :width: 400

In this window, you are able to perform a test to ensure parity with the schematic and the manufacturability of your design.

KiCAD's default selected tests are sane, and messing around with them is not recommended. All you have to do is press the `Run DRC` button and let it do its magic.

If your PCB fails, like this example, KiCAD will tell you what you need to fix. If you submit a failing design, your submission will be **auto-rejected**.

.. image:: img/icad_OvKKx1TbyM.png
  :width: 400

How to fix DRC?
---------------

In your main project directory, alongside your kicad_pcb and kicad_sch files, drop the following (file)[assets/JLCPCB.kicad_dru], and name it like the rest of your project.

This file automatically tells KiCAD the capabilities of JLCPCB, a fan-favorite PCB fabricator. If you go with a different fabrication plant for your final design, you will have to select different design rules. 