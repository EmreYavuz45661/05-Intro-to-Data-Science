# 05-Intro-to-Data-Science
Intro to data science for BWSI-Remote Sensing

## Exercise
Students will download a .csv with 450,000+ rows with the following columns. Using Python, student will be asked to analyze the data and produce statistics and an a GIS analysis of their choosing. Unlike previous exercises, students will need to create their own Colab /  Jupyter Notebooks.

### Data descriptions
| Column | Description |
|---------|--------------|
| FILENAME | Full file path of image |
| LAT_deg | Latitude in degrees |
| LON_deg | Longitude in degrees |
| ELEVATION_m_agl | Elevation above ground level in meters |
| YEAR | Calendar year photo was taken |
| MONTH | Calendar month photo was taken |
| DAY | Calendar day photo was taken |
| HOUR | Hour that photo was taken |
| MINUTE | Minute that photo was taken |
| SECOND | Second that photo was taken |
| STATEFP | US Census state code |
| COUNTYFP | US Census county code |
| COUNTYNS | US Census county code |
| GEOID | US Census geoid |
| KOPPEN | Köppen-Geiger climate classification |

### Load data into Google Colab from local file
This code snippet will prompt the user to upload a file in Google Colab.
```python
from google.colab import files
uploaded = files.upload()
```

### Store data in a in a Pandas Dataframe
This code snippet can be used to load the upload file as a Pandas dataframe.
```python
import io
import pandas
data = pandas.read_csv(io.BytesIO(uploaded['FILENAME.csv']))
```

## Supplemental MIT OCW Lectures
MIT OpenCourseWare (OCW) is a web-based publication of virtually all MIT course content. OCW is open and available to the world and is a permanent MIT activity. Here is a list of OCW video lectures related to this course content.

### ESD.051J: 10-Step Design Process and Dieter Ram
[![OCW.051J](http://img.youtube.com/vi/KPWMFrMA52Y/0.jpg)](http://www.youtube.com/watch?v=KPWMFrMA52Y "10-Step Design Process and Dieter Ram (Sample Lecture)")

### 6.0002: Clustering
[![OCW6.0002](http://img.youtube.com/vi/esmzYhuFnds/0.jpg)](http://www.youtube.com/watch?v=esmzYhuFnds "Clustering")

### 6.041: Counting
[![OCW6.041](http://img.youtube.com/vi/6oV3pKLgW2I/0.jpg)](http://www.youtube.com/watch?v=6oV3pKLgW2I "Counting")

## References
### MIT OCW
Eric Grimson, John Guttag, and Ana Bell. [6.0002 Introduction to Computational Thinking and Data Science.](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-0002-introduction-to-computational-thinking-and-data-science-fall-2016/index.htm) Fall 2016. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA.

Blade Kotelly, and Joel Schindall. [ESD.051J Engineering Innovation and Design.](https://ocw.mit.edu/courses/engineering-systems-division/esd-051j-engineering-innovation-and-design-fall-2012/index.htm#) Fall 2012. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA. 

Andrew Sutherland. [Combinatorics: The Fine Art of Counting.](https://ocw.mit.edu/high-school/mathematics/combinatorics-the-fine-art-of-counting/index.htm#) Summer 2007. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA. 

John Tsitsiklis. [6.041 Probabilistic Systems Analysis and Applied Probability.](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-041-probabilistic-systems-analysis-and-applied-probability-fall-2010/index.htm#) Fall 2010. Massachusetts Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu. License: Creative Commons BY-NC-SA. 

### Data
Rubel, F., and M. Kottek, 2010: Observed and projected climate shifts 1901-2100 depicted by world maps of the Köppen-Geiger climate classification. Meteorol. Z., 19, 135-141. DOI: 10.1127/0941-2948/2010/0430.

[TIGER/Line Shapefile, 2018, nation, U.S., Current County and Equivalent National Shapefile](https://catalog.data.gov/dataset/tiger-line-shapefile-2018-nation-u-s-current-county-and-equivalent-national-shapefile)

## Distribution Statement
DISTRIBUTION STATEMENT A. Approved for public release. Distribution is unlimited.

(C) 2019 Massachusetts Institute of Technology.

Delivered to the U.S. Government with Unlimited Rights, as defined in DFARS Part 252.227-7013 or 7014 (Feb 2014). Notwithstanding any copyright notice, U.S. Government rights in this work are defined by DFARS 252.227-7013 or DFARS 252.227-7014 as detailed above. Use of this work other than as specifically authorized by the U.S. Government may violate any copyrights that exist in this work.
