---
layout: mfile
title: PsychColorimetricMatFiles
categories:
  - PsychColorimetricMatFiles
encoding: UTF-8
---

Psychtoolbox:PsychColorimetricData:PsychColorimetricMatFiles.

help PsychColorimetricData
help PsychColorimetric

This folder holds colorimetric data in .mat file form.
All data files are in a standard format.

A very useful source for on-line
colorimetric data is the CVRL database:
  http://cvrl.ioo.ucl.ac.uk/
Many of the functions used here were downloaded from
that source and then splined to the wavelength sampling
used here (with extension by zeros).

  B\_xxx files contain basis functions.  The basis functions themselves
    are in the columns of a matrix with name B\_xxx.  There is also
    a 3 by 1 row vector S\_xxx that contains the wavelength sampling
    information in the form [start delta numberSamples] where start
    and delta are in nanometers.

  den\_xxx files contain optical density data.  In log units.  To
    convert density values to transmittance, take 10^(-den).  There
    is also an S\_xxx vector.  Curiously, these are in column vectors
    in the .mat files.

  spd\_xxx files contain spectral power distributions.  Data are in
    columns of matrix with name spd\_xxx.  There is also a S\_xxx
    vector.

  sur\_xxx files contain surface reflectance functions (range 0-1).  Data
    are in columns of matrix with name sur\_xxx.  There is also an S\_xxx
    vector.

  T\_xxx contain color matching functions or spectral sensitivities.  Data
     are in rows of a matrix with name T\_xxx.  There is also an S\_xxx
     vector.  All are in energy units, so that multiplying by spectra in
     energy (not quanta) gives desired result (often proportional to
     isomerization rate).

 Specific data files are listed below.  Most, but not all, are sampled
 between 380 nm and 780 nm at 5 nm intervals (S = [380 5 81]).  This is
 the CIE standard.  Good coding practice requires using the S\_xxx vector
 loaded with the data and splining to the wavelength sampling you want to work
 in.  If I were to start this database again, I would have kept each function
 at the resolution of its source.

 In some cases, the original data were interpolated or extraploated (with zeros)
 to put them data onto the CIE standard [380 5 81] wavelength.

 See also: EnergyToQuanta, QuantaToEnergy, MakeItS, MakeItWls, MakeItStruct,
   SplineSpd, SplineSrf, SplineCmf.

  B\_cieday            - CIE daylight basis functions.
  B\_cohen             - Cohens basis functions for Munsell surfaces.
  B\_monitor           - Basis functions for a color monitor.
  B\_nickerson         - Basis functions for Munsell surfaces.
  B\_roomillum         - Basis functions for illuminants in Brainard's room.
  B\_vrhel             - Basis functions for Vrhel surface measurements.
  den\_lens\_ws         - Relative lens density data (re 700 nm).  W&S, Table 1(2.4.6), p. 109.
                      -   This is the first data set in the table, not the Norren and Vos
                      -   data.  It is for an open pupil.
  den\_lens\_cie\_1      - Part one of CIE component lens density function. CIE 170-1:2006, Table 6.10
  den\_lens\_cie\_2      - Part two of CIE component lens density function. CIE 170-1:2006, Table 6.10
  den\_lens\_ssf        - Stockman-Sharpe-Fach (1999) lens optical density spectrum.
                      -   See CVRL database, CIE 170-1:2006, Table 6.10, 32 yo, pupil \<= 3 degrees.
                      -   This is also the sum of den\_lens\_cie\_1 and den\_lens\_cie\_2
  den\_mac\_bone        - Macular pigment density from Bone et al. (1992).  See CVRL database, CIE 170-1:2006, Table 6.4, 2-deg.
  den\_mac\_vos         - Macular pigment density from Vos.  See CVRL database.
  den\_mac\_ws          - Macular pigment density from W&S, Table 2(2.4.6), p. 112.
  spd\_appratusrel     - Relative spectrum from a monitor.  Used by IsomerizationInDishDemo.
  spd\_CIEA            - Spectral power distribtion for CIE illuminant A.
  spd\_CIEC            - Spectral power distribution for CIE illuminant C.
  spd\_D65             - Spectral power distribution for CIE illuminant D65.
  spd\_flourescent     - Spectral power distribution for some flourescent lamp.
  spd\_incanCC         - Spectral power distribution for some incandescent lamp.
  spd\_phillybright    - Direct bright sunlight measured through window and off of a piece of white paper towel
                      -   on the floor of DB's office in Philly, March 2013.
                      -   Measurements made with PR-650, power in Watts/[m2-sr-wlband].
  spd\_xenonArc        - Spectral power distribution for some xenon arc lamp.
  spd\_xenonFlash      - Spectral power distribuiton for some xenon flash tube.
  sur\_nickerson       - The Nickerson measurements of the Munsell papers.
  sur\_macbeth         - Reflectance of Macbeth color checker (not accurate, needs updating).
  sur\_vrhel           - Reflectances measured by Vrhel.
  T\_CIE\_Y2            - CIE physiologically relevant 2-degree luminosity function.  See CVRL database.
  T\_CIE\_Y10           - CIE physiologically relevant 10-degree luminosity function.  See CVRL database.
  T\_cones\_smj         - Stockman-MacLeod-Johnson cone fundamentals.  See CVRL database.
  T\_cones\_smj10       - Stockman-MacLeod-Johnson 10-degree cone fundamentals.  See CVRL database.
  T\_cones\_ss2         - Stockman-Sharpe (2000) 2-degree cone fundamentals.  See CVRL database.
  T\_cones\_ss10        - Stockman-Sharpe (2000) 10-degree cone fundamentals.  See CVRL database.
  T\_cones\_sp          - Smith-Pokorny cone fundamentals.  Specified between 380 and 780 nm, but non-zero only between 400 and 700 nm.
                      -   This is probably because these were typed in by hand long ago from a table that only had data between 400 and 700 nm
                      -   and then zero extended to match the wavelength sampling of other data files.
                      -   It might be good to update these with data over the full specified range.
  T\_DCS200            - Sensitivities of a Kodak DCS-200 color camera.
  T\_ground            - Not entirely sure what this is, but it might be ground squirrel receptor sensitivities.
  T\_Lanom             - Demarco et al. anomolous L cone sensitivity.
  T\_log10coneabsorbance\_ss - Stockman-Sharpe (2000) log10 LMS cone photopigment absorbance.
                      -   See CVRL database, CIE 170-1:2006, Table 6.6.
                      -   Some S-cone values were unspecified for wls \> 615 nm in the table.
                      -   These were filled in here by linear extrapolation.
                      -   Note that you want to raise 10 to these numbers
                      -   to get absorbance, which itself is a log-like quantity.
  T\_Manom             - Demarco et al. anomolous M cone sensitivity.
  T\_photopigments\_ss  - Removed.  Use T\_log10coneabsorbance and raise 10 to it.
  T\_melanopsin        - Melanopsin fundamental as provided by Lucas at
                      -   http://lucasgroup.lab.ls.manchester.ac.uk/research/measuringmelanopicilluminance/
                      -   This is for human observers at the cornea, in energy units.  Normalized to peak
                      -   of unity.
  T\_rods              - CIE scotopic luminous efficiency function.
  T\_stiles2           - Stiles 2-degree color matching functions.
  T\_ss2000\_Y2         - Stockman-Sharpe (2000) 2-degree photopic luminance efficiency function.  See CVRL database.
  T\_vos1978\_Y         - Judd-Vos 1978 photopic luminance efficiency function.
  T\_xyz1931           - CIE 1931 color matching functions.
  T\_xyz1964           - CIE 1964 supplemental color matching functions.
  T\_xyzJuddVos        - Judd-Vos modified color matching functions.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychColorimetricData/PsychColorimetricMatFiles/Contents.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychColorimetricData/PsychColorimetricMatFiles/Contents.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychColorimetricData/PsychColorimetricMatFiles/Contents.m</code>
</div>
