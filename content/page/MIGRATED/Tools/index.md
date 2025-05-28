---
title: Tools
banner: true
---

import GitHubIcon from '@mui/icons-material/GitHub'
import TerminalIcon from '@mui/icons-material/Terminal'
import WrenchIcon from '@mui/icons-material/Build'
import DesktopIcon from '@mui/icons-material/Computer'

<Image src="/images/rc/tool.png" float="left" />
[Contributors](https://github.com/Riverscapes) to the RC have been prolific in developing and vetting the science and theoretical underpinnings essential to understanding and explaining how riverscapes work and are organized across a range of nested hierarchical spatial scales. We have also committed to building [open-source algorithms](https://github.com/Riverscapes) {/* ICON: fa-github */} tools to make it easier for researchers, professionals, practitioners, and students to apply those concepts to their riverscapes and disseminate [FAIR](https://www.go-fair.org/fair-principles/) tools and [outputs from those tools](https://riverscapes.net/Tools/Technical_Reference/Documentation_Standards/Riverscapes_Projects/).

<Stack direction="row" spacing={2}>
  <Button to="https://tools.riverscapes.net/" imageSrc="/images/tools/grade/TRL_6_32p.png">
    Learn more about RC's **Production-Grade Network-Scale Tools**
  </Button>

  <Button to="https://github.com/Riverscapes" iconName="GitHubIcon" >
    RC **Open Source** Tools on Github
  </Button>

  <Button to="/Tools/toolStandards.html" imageSrc="/images/rc/RiverscapesCompliant_32.png">
      Learn more about RC-Compliant **Tool Standards** <WrenchIcon />
  </Button>
</Stack>

# Riverscapes Compliant

<Image noWrap src="/images/rc/RiverscapesCompliant_128.png" float="right" />

Tools are designated as "*riverscapes-compliant*" when they meet the following criteria:
- [Tool Status](/Tools/discrimination#tool-grade) of **Operational-Grade** or Higher
- Code produces [riverscapes projects](/Tools/Technical_Reference/Documentation_Standards/Riverscapes_Projects/) <Image noWrap src="/images/data/RiverscapesProject_24.png" /> as output of all analyses
- Project Type is registered with [`program.xml`](/Tools/Technical_Reference/Documentation_Standards/Riverscapes_Projects/Program/) in [Program Repo](https://github.com/Riverscapes/RiverscapesXML)
- Source-Code is open-source and [FAIR](https://force11.org/info/the-fair-data-principles/)
- Has been vetted by the RS Science Committee (i.e. has a "[Report Card](/Tools/reportcards.html)")

------------------

## Riverscapes Compliant Tools

All tools ranked as RC-Compliant <Image noWrap src="/images/rc/RiverscapesCompliant_24.png" /> are based on peer-reviewed methods and have been additionally vetted by our RS Science Committee. When RC developers have developed new methods themselves, the RC encourages peer vetting, publication, and dissemination in the peer-reviewed literature. The RC also makes sure to have a well-documented website (typically with a URL that will take the form of `sometool.riverscapes.net`). For most users, the online help documentation and using the [tool](/Tools) 'as is' is as far as they need to take it. However, for those so inclined, all of the underlying source-code for these tools, models, and algorithms are available in their GitHub {/* ICON: fa-github */} repository at [github.com/Riverscapes](https://github.com/Riverscapes). Note that the [`tools.riverscapes.net`](https://github.com/Riverscapes/riverscapes-tools/tree/master/lib/commons)`/sometool` convention is used for our predominantly [production-grade tools](http://tools.riverscapes.net) that share the [`Riverscapes Commons` Library](https://github.com/Riverscapes/riverscapes-tools/tree/master/lib/commons).

| | Resolution | Extent | Language | Interface | Status |
| --- | --- | --- | --- | --- | --- |
| Exploratory Tools for Visualizing Riverscapes Projects | | | | | |
| [WebRAVE](http://rave.riverscapes.net/) | Any | Any | react, javascript | {/* ICON: fa-chrome */} & <Image noWrap src="/images/data/api_24.png" /> | Commercial Grade <Image noWrap src="/images/tools/grade/TRL_7_32p.png" /> |
| [QRAVE](http://rave.riverscapes.net/) | Any | Any | Python | <Image noWrap src="/images/tools/QGIS_bw_24.png" /> | Professional-Grade <Image noWrap src="/images/tools/grade/TRL_4_32p.png" /> |
| [ArcRAVE](http://rave.riverscapes.net/) | Any | Any | C# | <Image noWrap src="/images/tools/esri_icon.png" /> | Professional-Grade <Image noWrap src="/images/tools/grade/TRL_4_32p.png" /> |
| Reach Scale Tools | | | | | |
| [GCD - Geomorphic Change Detection](http://gcd.riverscapes.net/) | Cell | Reach | C# | <DesktopIcon /> , <Image noWrap src="/images/tools/esri_icon.png" />, <TerminalIcon /> | [Professional-Grade](https://gcd.riverscapes.net/About/Status/Tool_ReportCard_7-5-00.html) <Image noWrap src="/images/tools/grade/TRL_4_32p.png" /> for <DesktopIcon /> & <Image noWrap src="/images/tools/esri_icon.png" />; <br>Production-Grade for CLI <TerminalIcon /> |
| [GUT - Geomorphic Unit Toolkit](http://gut.riverscapes.net/) | Cell | Reach | Python | <TerminalIcon />, <Image noWrap src="/images/tools/ArcPyToolbox.png" /> | Research-Grade |
| [FHM - Fish Habitat Model](http://habitat.northarrowresearch.com/) | Cell | Reach | C#/C++ | <DesktopIcon /> | Operational-Grade |
| Network Scale Tools | | | | | |
| [Riverscapes Context](http://tools.riverscapes.net/rscontext) - RS_Context 1.2.2 | Reach | Network | Python | <TerminalIcon /> | [Production-Grade](https://tools.riverscapes.net/rscontext/Status/ReportCard_1.2.2.html) <Image noWrap src="/images/tools/grade/TRL_6_32p.png" /> |
| [Channel Area Tool](http://tools.riverscapes.net/channel) 1.1.1 | Reach | Network | Python | <TerminalIcon /> | [Production-Grade](https://tools.riverscapes.net/channel/Status/ReportCard_1.1.1.html) <Image noWrap src="/images/tools/grade/TRL_6_32p.png" /> |
| [TauDEM - Terrain Analysis Using Digital Elevation Models](http://tools.riverscapes.net/taudem) - TauDEM 1.0.2 | Reach | Network | Python | <TerminalIcon /> | [Production-Grade](https://tools.riverscapes.net/taudem/Status/ReportCard_1.0.2.html) <Image noWrap src="/images/tools/grade/TRL_6_32p.png" /> |
| [VBET - Valley Bottom Extraction Tool](http://tools.riverscapes.net/vbet) - VBET 0.5.1 Beta | Reach | Network | Python | <TerminalIcon /> | [Production-Grade](https://tools.riverscapes.net/vbet/Status/ReportCard_0.5.1.html) <Image noWrap src="/images/tools/grade/TRL_6_32p.png" /> |
| [BRAT - Beaver Restoration Assessment Tool](http://tools.riverscapes.net/brat) - sqlBRAT 4.3.2 | Reach | Network | Python | <TerminalIcon /> | [Production-Grade](http://tools.riverscapes.net/brat/About/Status/ReportCard_4.3.2.html) <Image noWrap src="/images/tools/grade/TRL_6_32p.png" /> |
| [pyBRAT - Beaver Restoration Assessment Tool](http://brat.riverscapes.net/) - pyBRAT 3.1.0 | Reach | Network | Python | <Image noWrap src="/images/tools/ArcPyToolbox.png" /> | [Operational-Grade](http://brat.riverscapes.net/Documentation/Status/Tool_ReportCard_3-1-00) <Image noWrap src="/images/tools/grade/TRL_4_32p.png" /> |
| [RCAT - Riparian Condition Assessment Tool](http://rcat.riverscapes.net/) | Reach | Network | Python | <Image noWrap src="/images/tools/ArcPyToolbox.png" /> | Research-Grade |
| [GNAT - Geomorphic Network Assessment Tool](http://gnat.riverscapes.net/) | Reach | Network | Python | <Image noWrap src="/images/tools/ArcPyToolbox.png" /> | Research-Grade |
| Legacy CHaMP Tools | | | | | |
| [CHaMP Topo Processing Tools](http://champtools.northarrowresearch.com/) | Reach | Reach | Python | <Image noWrap src="/images/tools/esri_icon.png" /> | Production-Grade |
| [CHaMP Topo Metrics](https://github.com/SouthForkResearch/CHaMP_Metrics/wiki) | Reach | Network | Python | <Image noWrap src="/images/tools/ArcPyToolbox.png" /> | Production-Grade |

-----

## Tools Pending Riverscapes Compliance

<Image src="/images/rc/RiverscapesCompliantPending_128.png" float="right" />

Tools are designated as "*pending riverscapes-compliance*" <Image noWrap src="/images/rc/RiverscapesCompliantPending_28.png" /> when the RS Science Committee has accepted the tool for consideration and they meet the following criteria:
- [Tool Status](/Tools/discrimination#tool-grade) of **Resarch-Grade** or higher
- Developer has indicated intent to modify code to produce [riverscapes projects](/Tools/Technical_Reference/Documentation_Standards/Riverscapes_Projects/) as output of all analyses - Moving up to **Operational-Grade**
- Developer has indicated intent to add Project Type registration with [`program.xml`](/Tools/Technical_Reference/Documentation_Standards/Riverscapes_Projects/Program/) in [Program Repo](https://github.com/Riverscapes/RiverscapesXML)

| | Resolution | Extent | Language | Interface | Status |
| --- | --- | --- | --- | --- | --- |
| Tools for doing your own Riverscapes Analyses | | | | | |
| [Riverscape Studio - for QGIS (QRiS)](http://qris.riverscapes.net/) | Any | Riverscape | Python | <Image noWrap src="/images/tools/QGIS_bw_24.png" /> | Professional-Grade <Image noWrap src="/images/tools/grade/TRL_4_32p.png" /> |
| Reach Scale Tools | | | | | |
| [Fluvial Corridor Toolbox](https://github.com/EVS-GIS/Fluvial-Corridor-Toolbox-ArcGIS) | Cell | Reach | Python | <Image noWrap src="/images/tools/ArcPyToolbox.png" /> , <Image noWrap src="/images/tools/QGIS_bw_24.png" /> | Operational-Grade |
| [MoRPHED - Model of Riverine Physical Habitat & Ecogeomorphic Dynamics](http://morphed.joewheaton.org/) | Cell | Reach | C++ | <DesktopIcon /> | Research-Grade |
| [NREI - Net Rate of Energy Intake](https://github.com/Riverscapes/NREI) | Cell | Reach | R | <TerminalIcon /> | Research-Grade |
| [RIM - Riverscapes Inundation Mapper Tool](https://rim.riverscapes.net) | Cell | Reach | Python | <TerminalIcon /> | <Image noWrap src="/images/tools/grade/TRL_3_32p.png" />[Research-Grade](https://rim.riverscapes.net/About/Status/Tool_ReportCard_0-1-00.html) |
| [TAT - Topographic Analyis Toolkit](https://tat.riverscapes.net) | Cell | Reach | Python | <Image noWrap src="/images/tools/esri_icon.png" /> | Operational-Grade |
| [ToPCAT - Topographic Point Cloud Analysis Toolkit](http://tat.riverscapes.net/Help/Analysis/roughness-analysis-submenu/simple-topcat-roughness.html) | Cell | Reach | C++ | <Image noWrap src="/images/tools/esri_icon.png" /> | Research-Grade |
| Network Scale Tools | | | | | |
| [CASCADE Toolbox](http://cascade.deib.polimi.it/) | Reach | Network | Matlab | <DesktopIcon /> | Opperational-Grade |
| [Catchment Tool](https://riverscapes.github.io/CatchmentTool/) | Reach | Network | Python | <Image noWrap src="/images/tools/ArcPyToolbox.png" /> | Research-Grade |
| [Conductivity Tools](https://riverscapes.github.io/Conductivity/) | Reach | Network | Python | <Image noWrap src="/images/tools/ArcPyToolbox.png" /> | Research-Grade |
| [GNAT - Geomorphic Network Assessment Tool](http://gnat.riverscapes.net/) | Reach | Network | Python | <Image noWrap src="/images/tools/ArcPyToolbox.png" /> | Research-Grade |
| [Grain Size Tool](https://github.com/Riverscapes/grain-size-tool) | Reach | Network | Python | <Image noWrap src="/images/tools/ArcPyToolbox.png" /> | Research-Grade |
| [Network Profiler Tool](https://riverscapes.github.io/NetworkProfiler/) | Reach | Network | Python | <Image noWrap src="/images/tools/QGIS_bw_24.png" /> | Research-Grade |
| [Solar Stream Tools](https://riverscapes.github.io/SolarStream/) | Reach | Network | Python | <Image noWrap src="/images/tools/ArcPyToolbox.png" /> | Research-Grade |
| [Tributary Impact](http://tributaryimpact.riverscapes.net/) | Reach | Network | Python | <Image noWrap src="/images/tools/ArcPyToolbox.png" /> | Proof of Concept |
| [WRAT - Wood Restoration Assessment Tool](https://github.com/Riverscapes/WRAT) | Reach | Network | Python | <Image noWrap src="/images/tools/ArcPyToolbox.png" /> | Proof of Concept |
| Catchment Scale Tools | | | | | |
| [Connectivity Index](https://github.com/HydrogeomorphologyTools/Connectivity-Index-ArcGIS-toolbox) | Cell | Catchment | Python | <Image noWrap src="/images/tools/ArcPyToolbox.png" /> | Research-Grade |
| [Tributary Impact](http://tributaryimpact.riverscapes.net/) | Reach | Network | Python | <Image noWrap src="/images/tools/ArcPyToolbox.png" /> | Proof of Concept |
| [WRAT - Wood Restoration Assessment Tool](https://github.com/Riverscapes/WRAT) | Reach | Network | Python | <Image noWrap src="/images/tools/ArcPyToolbox.png" /> | Proof of Concept |
| Catchment Scale Tools | | | | | |
| [Connectivity Index](https://github.com/HydrogeomorphologyTools/Connectivity-Index-ArcGIS-toolbox) | Cell | Catchment | Python | <Image noWrap src="/images/tools/ArcPyToolbox.png" /> | Research-Grade |
| [SedInConnect](https://github.com/HydrogeomorphologyTools/SedInConnect_2.3) | Cell | Catchment | Python | <DesktopIcon /> | Operational-Grade |
| Utilities | | | | | |
| [PointCloud2Raster](https://github.com/NorthArrowResearch/pointcloud2raster) | Point | Reach | C++ | <TerminalIcon /> | Proof of Concept |
| [PySESA - Spatially Explicit Spectral Analysis](https://github.com/dbuscombe-usgs/pysesa) | Point | Reach | Python | <TerminalIcon /> | Research-Grade |
| [RasterMan](https://github.com/NorthArrowResearch/rasterman) | Cell | Catchment | C++ | <TerminalIcon /> | Research-Grade |
| Legacy CHaMP Tools | | | | | |
| [CTT - CHaMP Transformation Tool](http://ctt.riverscapes.net/index.html) | Cell | Reach | C# | <Image noWrap src="/images/tools/esri_icon.png" /> | Operational-Grade |
| [CHaMP Topo Processing Tools](http://champtools.northarrowresearch.com/) | Reach | Reach | Python | <DesktopIcon /> | Operational-Grade |
| [CHaMP Workbench](http://workbench.northarrowresearch.com/) | Any | Any | C# | <DesktopIcon /> | Professional-Grade |
| [CHaMP Hydraylic-Modelling Delft3D Automation](https://github.com/SouthForkResearch/Hydraulic-Modeling/wiki) | Cell | Reach | R/C | <TerminalIcon /> | Research-Grade |

----------

#### [Model Discrimination](/Tools/discrimination)

We discriminate our tools based on their [interface](/Tools/discrimination#interface) and [tool grade](/tools/discrimination#tool-grade).

<Stack align="center">

<Button to="/discrimination#interface" imageSrc="/images/tools/grade/TRL_1_32p.png">
  Learn more about RC's **Tool Interface**
</Button>


</Stack>

##### Tool Grade

We classify the [grade](/Tools/discrimination#tool-grade) of our tools according to their growth from innovative research ideas, through to operational tools in development that (with a little love and patience) can be run by someone other than the developer, on through to more broadly deployable professional tools that are robust and usable by any user in very different settings.
