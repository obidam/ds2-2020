# Projects Guidline

## Github Procedure
- Fork this github repository to your own account
- Add a folder under ds2-2020/projects, name it with your last name
- Work out your project codes/documentation and stage/push it to your folder
- Once finalized, create a pull request to the main branch

## Projects #5: Ocean warming
 
*Description*: Because of the human driven intensification of the greenhouse effect, the ocean is warming. 
You can compute ocean heat content (OHC) and its trend with a regression (linear or not) for the entire ocean time 
series and extrapolate to the future, e.g. what is the expected ocean warming for the horizon 2100.

Instead of working globally, you can study the ocean warming locally. In that case, you can plot the local slopes of 
the different OHC time series and deduce where the ocean warming is moderate and where it is strong.

*Data*: You will use the [EN4 dataset](https://www.metoffice.gov.uk/hadobs/en4/) that is an interpolation of all available
ocean observations (of temperature and salinity) onto a regular space/time grid.

This dataset can be accessed this way:

    fs = gcsfs.GCSFileSystem(project="alert-ground-261008")
    gcsmap = fs.get_mapper("opendata_bdo2020/EN.4.2.1.f.analysis.g10.zarr")
    ds = xr.open_zarr(gcsmap)
    

## Projects #6: Ocean warming contribution to Sea level rise
 
*Description*: Sea level increases because of changes in currents (dynamic effect) and because of ocean density changes 
(steric effect). Compute ocean density changes contribution to Sea level rises (thermosteric effect) and demonstrate 
that it is the driver of regional sea level change trends.
 
*Data*: You will use the [EN4 dataset](https://www.metoffice.gov.uk/hadobs/en4/) that is an interpolation of all available
ocean observations (of temperature and salinity) onto a regular space/time grid.

This dataset can be accessed this way:

    fs = gcsfs.GCSFileSystem(project="alert-ground-261008")
    gcsmap = fs.get_mapper("opendata_bdo2020/EN.4.2.1.f.analysis.g10.zarr")
    ds = xr.open_zarr(gcsmap)    
