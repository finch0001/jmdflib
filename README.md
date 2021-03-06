# jMDFLib [![Build Status](https://travis-ci.org/wollekuel/jmdflib.svg?branch=master)](https://travis-ci.org/wollekuel/jmdflib)

I'm thinking about doing a re-implementation of [jMDFLib](https://sourceforge.net/projects/jmdflib/).

I'm using Vector's specification document for version 3.1.1, accessible from their [homepage](https://vector.com/downloads/mdf_specification.pdf). Unfortunately, no newer specification files are available...

## Status

### Implemented block types

* IDBlock
* HDBlock
* TXBlock
* DGBlock
* CGBlock
* CNBlock
* CCBlock (partially)

#### Not tested

* More than one DGBlock
* More than one CGBlock

### Missing block types

* All other

## Missing implementations

* Files lenghts greater or equal than `Integer.MAX_VALUE`
* Unfinalized MDF files
* Big Endian byte order
* Floating-point format compliant with G_Float or D_Float
* PRBlock
* Number of Record IDs > 0
* TRBlock (only preparation exists)
* Signal data type != `IEEE_754_FLOATING_POINT_FORMAT`
* CCBlock
	* Tabular with interpolation
	* Tabular
	* Polynomial function
	* Exponential function
	* Logarithmic function
	* Rational conversion formula
	* ASAM-MCD2 Text formula
	* ASAM-MCD2 Text table, (COMPU_VTAB)
	* ASAM-MCD2 Text Range table (COMPU_VTAB_RANGE)
	* Date
	* Time
* CEBlock
* CDBlock
* Reading data
	* Data records with record IDs
	* Start offset % 8 bits != 0