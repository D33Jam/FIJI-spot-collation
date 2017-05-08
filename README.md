# FIJI-spot-collation
FIJI macro used for assembling spots from multiple stacks into  single stacks for analysis
 W. David. Jamieson 05-05-2017 ImageJ version number:FIJI ImageJ 1.51K  //
////////////////////////////////////////////////////////////////////////////
//This Macro  is used to take spots from several image splitter t-stacks    
// (512*512 image top 256 laser bottom 256 fluorescence)					
//where one channel represents the laser spot and the other the fluorescence,
// and aggregate them into a single stack through addition.					
//The process proceeds is several distinct steps:							
// 1. You are asked to pick first a directory where stacks to be processed	
//    can be located and then a directory where results are to be saved.	
// 2. An image is generated and you are asked to pick:						
//   		-The number of spots											
//   		-Their approximate size											
//   		-The approximate space between them								
// 3. The image undergoes correction for laser spot movement, sample		
//	  inhomogeneity, laser power fluctuation.								
// 4. Spots are picked based on find maximum within pre-defined subregions	
//    (to account for X/Y drift).											
// 5. Spots are summed in to t-stacked aggregates as a way to amplify signal
