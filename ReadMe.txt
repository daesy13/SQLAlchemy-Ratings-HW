{\rtf1\ansi\ansicpg1252\cocoartf1561\cocoasubrtf600
{\fonttbl\f0\fswiss\fcharset0 Helvetica;\f1\fnil\fcharset0 AndaleMono;\f2\fmodern\fcharset0 Courier;
\f3\fmodern\fcharset0 Courier-Bold;\f4\fmodern\fcharset0 Courier-Oblique;}
{\colortbl;\red255\green255\blue255;\red0\green0\blue0;\red213\green213\blue213;\red38\green38\blue38;
\red255\green255\blue11;\red208\green149\blue26;\red193\green193\blue193;\red222\green53\blue46;\red50\green91\blue142;
\red13\green95\blue24;\red29\green111\blue63;\red83\green83\blue83;\red51\green109\blue125;\red0\green0\blue233;
\red255\green255\blue255;\red94\green141\blue197;}
{\*\expandedcolortbl;;\cssrgb\c0\c0\c0;\cssrgb\c86667\c86667\c86667;\cssrgb\c20000\c20000\c20000;
\cssrgb\c100000\c100000\c0;\cssrgb\c85490\c64706\c12549;\cssrgb\c80000\c80000\c80000;\cssrgb\c90588\c29804\c23529;\cssrgb\c25098\c43922\c62745;
\cssrgb\c0\c43922\c12549;\cssrgb\c12549\c50196\c31373;\cssrgb\c40000\c40000\c40000;\cssrgb\c25098\c50196\c56471;\cssrgb\c0\c0\c93333;
\cssrgb\c100000\c100000\c100000;\cssrgb\c43922\c62745\c81569;}
{\*\listtable{\list\listtemplateid1\listhybrid{\listlevel\levelnfc23\levelnfcn23\leveljc0\leveljcn0\levelfollow0\levelstartat1\levelspace360\levelindent0{\*\levelmarker \{disc\}}{\leveltext\leveltemplateid1\'01\uc0\u8226 ;}{\levelnumbers;}\fi-360\li720\lin720 }{\listname ;}\listid1}
{\list\listtemplateid2\listhybrid{\listlevel\levelnfc0\levelnfcn0\leveljc0\leveljcn0\levelfollow0\levelstartat1\levelspace360\levelindent0{\*\levelmarker \{decimal\}.}{\leveltext\leveltemplateid101\'02\'00.;}{\levelnumbers\'01;}\fi-360\li720\lin720 }{\listname ;}\listid2}
{\list\listtemplateid3\listhybrid{\listlevel\levelnfc23\levelnfcn23\leveljc0\leveljcn0\levelfollow0\levelstartat1\levelspace360\levelindent0{\*\levelmarker \{disc\}}{\leveltext\leveltemplateid201\'01\uc0\u8226 ;}{\levelnumbers;}\fi-360\li720\lin720 }{\listname ;}\listid3}}
{\*\listoverridetable{\listoverride\listid1\listoverridecount0\ls1}{\listoverride\listid2\listoverridecount0\ls2}{\listoverride\listid3\listoverridecount0\ls3}}
\margl1440\margr1440\vieww10800\viewh8400\viewkind0
\deftab720
\pard\pardeftab720\sl420\sa298\partightenfactor0

\f0\b\fs36 \cf2 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Setup\
\pard\pardeftab720\sl280\sa240\partightenfactor0

\b0\fs24 \cf2 There are a number of Python libraries we\'92ll need for this project.\
We\'92ll create a virtual environment and install them, using a\'a0
\i\b requirements.txt
\i0\b0 \'a0file that has the names and exact versions of products we\'92d like to use:\
\pard\pardeftab720\sl360\partightenfactor0

\f1 \cf3 \cb4 \strokec3 $ \cf5 \strokec5 virtualenv\cf3 \strokec3  \cf5 \strokec5 env\cf3 \strokec3 \
New python executable in env/bin/python\
Installing setuptools, pip...done.\
$ \cf5 \strokec5 source env/bin/activate\cf3 \strokec3 \
(env) $ \cf5 \strokec5 pip3\cf3 \strokec3  \cf5 \strokec5 install -r requirements.txt\cf3 \strokec3 \
Downloading/unpacking Flask (from -r requirements.txt (line 1))\
Downloading Flask-0.10.1.tar.gz (544kB): 544kB downloaded\
\pard\pardeftab720\sl360\partightenfactor0
\cf6 \strokec6 ...\cf3 \strokec3 \
\
Successfully installed Flask Flask-SQLAlchemy Jinja2 \cf6 \strokec6 ...\cf3 \strokec3 \
Cleaning up...\
(env) $\
\pard\pardeftab720\sl280\sa240\partightenfactor0

\f0 \cf2 \cb1 \strokec2 Awesome.\
\pard\pardeftab720\sl280\partightenfactor0
\cf2 \
\pard\pardeftab720\sl420\sa298\partightenfactor0

\b\fs36 \cf2 Building the Database\
\pard\pardeftab720\sl280\sa240\partightenfactor0

\b0\fs24 \cf2 Okay, so our data is in files and we need to put them into database tables. Great, we\'92ll start writing a schema. Identify the tables we\'92ll need to make, and sketch out the schema.\
We\'92re not going to use all the genre data for movies, nor are we going to keep track of users\'92 genders or occupations.\
However, we\'92ll add authentication data to the user schema, adding both an email and password, while making the remaining user data optional. Sketch out a rough schema as well as any relationships between the tables (has many, belongs to, etc).\
Going by our files, we can come up with the following skeleton:\
Model\
\pard\pardeftab720\sl280\sa240\partightenfactor0

\b \cf2 User
\b0 \

\itap1\trowd \taflags1 \trgaph108\trleft-108 \trbrdrt\brdrnil \trbrdrl\brdrnil \trbrdrr\brdrnil 
\clvertalb \clshdrawnil \clwWidth1027\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx4320
\clvertalb \clshdrawnil \clwWidth7049\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx8640
\pard\intbl\itap1\pardeftab720\sl280\qc\partightenfactor0

\b \cf2 Name\cell 
\pard\intbl\itap1\pardeftab720\sl280\qc\partightenfactor0
\cf2 Type\cell \row

\itap1\trowd \taflags1 \trgaph108\trleft-108 \trbrdrl\brdrnil \trbrdrr\brdrnil 
\clvertalt \clshdrawnil \clwWidth1027\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx4320
\clvertalt \clshdrawnil \clwWidth7049\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx8640
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0

\b0 \cf2 user_id\cell 
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0
\cf2 integer, primary key\cell \row

\itap1\trowd \taflags1 \trgaph108\trleft-108 \trbrdrl\brdrnil \trbrdrr\brdrnil 
\clvertalt \clshdrawnil \clwWidth1027\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx4320
\clvertalt \clshdrawnil \clwWidth7049\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx8640
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0
\cf2 email\cell 
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0
\cf2 optional string\cell \row

\itap1\trowd \taflags1 \trgaph108\trleft-108 \trbrdrl\brdrnil \trbrdrr\brdrnil 
\clvertalt \clshdrawnil \clwWidth1027\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx4320
\clvertalt \clshdrawnil \clwWidth7049\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx8640
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0
\cf2 password\cell 
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0
\cf2 optional string\cell \row

\itap1\trowd \taflags1 \trgaph108\trleft-108 \trbrdrl\brdrnil \trbrdrr\brdrnil 
\clvertalt \clshdrawnil \clwWidth1027\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx4320
\clvertalt \clshdrawnil \clwWidth7049\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx8640
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0
\cf2 age\cell 
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0
\cf2 optional integer\cell \row

\itap1\trowd \taflags1 \trgaph108\trleft-108 \trbrdrl\brdrnil \trbrdrb\brdrs\brdrw20\brdrcf7 \trbrdrr\brdrnil 
\clvertalt \clshdrawnil \clwWidth1027\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx4320
\clvertalt \clshdrawnil \clwWidth7049\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx8640
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0
\cf2 zipcode\cell 
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0
\cf2 optional string (technically, these aren\'92t numeric)\cell \lastrow\row
\pard\pardeftab720\sl280\sa240\partightenfactor0

\b \cf2 Movie
\b0 \

\itap1\trowd \taflags1 \trgaph108\trleft-108 \trbrdrt\brdrnil \trbrdrl\brdrnil \trbrdrr\brdrnil 
\clvertalb \clshdrawnil \clwWidth1254\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx4320
\clvertalb \clshdrawnil \clwWidth5816\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx8640
\pard\intbl\itap1\pardeftab720\sl280\qc\partightenfactor0

\b \cf2 Name\cell 
\pard\intbl\itap1\pardeftab720\sl280\qc\partightenfactor0
\cf2 Type\cell \row

\itap1\trowd \taflags1 \trgaph108\trleft-108 \trbrdrl\brdrnil \trbrdrr\brdrnil 
\clvertalt \clshdrawnil \clwWidth1254\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx4320
\clvertalt \clshdrawnil \clwWidth5816\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx8640
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0

\b0 \cf2 movie_id\cell 
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0
\cf2 integer, primary key\cell \row

\itap1\trowd \taflags1 \trgaph108\trleft-108 \trbrdrl\brdrnil \trbrdrr\brdrnil 
\clvertalt \clshdrawnil \clwWidth1254\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx4320
\clvertalt \clshdrawnil \clwWidth5816\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx8640
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0
\cf2 title\cell 
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0
\cf2 string\cell \row

\itap1\trowd \taflags1 \trgaph108\trleft-108 \trbrdrl\brdrnil \trbrdrr\brdrnil 
\clvertalt \clshdrawnil \clwWidth1254\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx4320
\clvertalt \clshdrawnil \clwWidth5816\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx8640
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0
\cf2 released_at\cell 
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0
\cf2 datetime\cell \row

\itap1\trowd \taflags1 \trgaph108\trleft-108 \trbrdrl\brdrnil \trbrdrb\brdrs\brdrw20\brdrcf7 \trbrdrr\brdrnil 
\clvertalt \clshdrawnil \clwWidth1254\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx4320
\clvertalt \clshdrawnil \clwWidth5816\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx8640
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0
\cf2 imdb_url\cell 
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0
\cf2 string\cell \lastrow\row
\pard\pardeftab720\sl280\sa240\partightenfactor0

\b \cf2 Rating
\b0 \

\itap1\trowd \taflags1 \trgaph108\trleft-108 \trbrdrt\brdrnil \trbrdrl\brdrnil \trbrdrr\brdrnil 
\clvertalb \clshdrawnil \clwWidth960\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx4320
\clvertalb \clshdrawnil \clwWidth4564\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx8640
\pard\intbl\itap1\pardeftab720\sl280\qc\partightenfactor0

\b \cf2 Name\cell 
\pard\intbl\itap1\pardeftab720\sl280\qc\partightenfactor0
\cf2 Type\cell \row

\itap1\trowd \taflags1 \trgaph108\trleft-108 \trbrdrl\brdrnil \trbrdrr\brdrnil 
\clvertalt \clshdrawnil \clwWidth960\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx4320
\clvertalt \clshdrawnil \clwWidth4564\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx8640
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0

\b0 \cf2 rating_id\cell 
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0
\cf2 integer, primary key\cell \row

\itap1\trowd \taflags1 \trgaph108\trleft-108 \trbrdrl\brdrnil \trbrdrr\brdrnil 
\clvertalt \clshdrawnil \clwWidth960\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx4320
\clvertalt \clshdrawnil \clwWidth4564\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx8640
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0
\cf2 movie_id\cell 
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0
\cf2 integer\cell \row

\itap1\trowd \taflags1 \trgaph108\trleft-108 \trbrdrl\brdrnil \trbrdrr\brdrnil 
\clvertalt \clshdrawnil \clwWidth960\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx4320
\clvertalt \clshdrawnil \clwWidth4564\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx8640
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0
\cf2 user_id\cell 
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0
\cf2 integer\cell \row

\itap1\trowd \taflags1 \trgaph108\trleft-108 \trbrdrl\brdrnil \trbrdrb\brdrs\brdrw20\brdrcf7 \trbrdrr\brdrnil 
\clvertalt \clshdrawnil \clwWidth960\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx4320
\clvertalt \clshdrawnil \clwWidth4564\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx8640
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0
\cf2 score\cell 
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0
\cf2 integer\cell \lastrow\row
\pard\pardeftab720\sl280\sa240\partightenfactor0

\b \cf2 Relationships
\b0 \
\pard\tx220\tx720\pardeftab720\li720\fi-720\sl280\sa120\partightenfactor0
\ls1\ilvl0\cf2 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 A user has many ratings\
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 A rating belongs to a user\
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 A movie has many ratings\
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 A rating belongs to a movie\
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 A user has many movies through ratings\
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 A movie has many users through ratingsIn our terminal window with the activated virtual environment, run your\'a0
\i\b model.py
\i0\b0 \'a0with the\'a0
\f2\fs28\fsmilli14400 \cf8 \strokec8 -i
\f0\fs24 \cf2 \strokec2 \'a0option:\
\pard\pardeftab720\sl360\partightenfactor0
\ls1\ilvl0
\f1 \cf3 \cb4 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec3 (env) $ \cf5 \strokec5 python3\cf3 \strokec3  \cf5 \strokec5 -i model.py\cf3 \strokec3 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec3 Connected to DB.\
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec3 >>>\
\pard\pardeftab720\sl280\sa240\partightenfactor0
\ls1\ilvl0
\f0 \cf2 \cb1 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 We\'92ve put some code at the bottom of the\'a0
\i\b model.py
\i0\b0 \'a0file already that connects to the database. Open a second terminal window and type:\
\pard\pardeftab720\sl360\partightenfactor0
\ls1\ilvl0
\f1 \cf3 \cb4 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec3 (env) $ \cf5 \strokec5 psql ratings\cf3 \strokec3 \
\pard\pardeftab720\sl280\sa240\partightenfactor0
\ls1\ilvl0
\f0 \cf2 \cb1 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 to verify that the\'a0
\i\b ratings
\i0\b0 \'a0database does not exist. You should see:\
\pard\pardeftab720\sl360\partightenfactor0
\ls1\ilvl0
\f1 \cf3 \cb4 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec3 psql: FATAL:  database \cf9 \strokec9 "ratings"\cf3 \strokec3  does \cf10 \strokec10 not\cf3 \strokec3  exist\
\pard\pardeftab720\sl280\sa240\partightenfactor0
\ls1\ilvl0
\f0 \cf2 \cb1 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Now in your terminal create your empty database by typing:\
\pard\pardeftab720\sl360\partightenfactor0
\ls1\ilvl0
\f1 \cf3 \cb4 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec3 (env) $ \cf5 \strokec5 createdb ratings\cf3 \strokec3 \
\pard\pardeftab720\sl280\sa240\partightenfactor0
\ls1\ilvl0
\f0 \cf2 \cb1 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Then, back in the same python console execute the method on the database connection that creates the tables:\
\pard\pardeftab720\sl360\partightenfactor0
\ls1\ilvl0
\f1 \cf3 \cb4 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec3 >>> \cf5 \strokec5 db.create_all()\cf3 \strokec3 \
\pard\pardeftab720\sl280\sa240\partightenfactor0
\ls1\ilvl0
\f0 \cf2 \cb1 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Back in your second window type:\
\pard\pardeftab720\sl360\partightenfactor0
\ls1\ilvl0
\f1 \cf3 \cb4 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec3 (env) $ \cf5 \strokec5 psql ratings\cf3 \strokec3 \
\pard\pardeftab720\sl280\sa240\partightenfactor0
\ls1\ilvl0
\f0 \cf2 \cb1 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 This time you should see something like:\
\pard\pardeftab720\sl360\partightenfactor0
\ls1\ilvl0
\f1 \cf3 \cb4 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec3 psql (\cf11 \strokec11 9.4\cf12 \strokec12 .\cf11 \strokec11 4\cf3 \strokec3 )\
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec3 Type \cf9 \strokec9 "help"\cf3 \strokec3  \cf10 \strokec10 for\cf3 \strokec3  help\cf12 \strokec12 .\cf3 \strokec3 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec3 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec3 ratings\cf12 \strokec12 =\cf13 \strokec13 #\cf3 \strokec3 \
\pard\pardeftab720\sl280\sa240\partightenfactor0
\ls1\ilvl0
\f0 \cf2 \cb1 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Enter\'a0
\f2\fs28\fsmilli14400 \cf8 \strokec8 \\d
\f0\fs24 \cf2 \strokec2 \'a0(the \'93d\'94 stands for \'93describe\'94) to see what tables are in the ratings database, and then\'a0
\f2\fs28\fsmilli14400 \cf8 \strokec8 \\d\'a0users
\f0\fs24 \cf2 \strokec2 \'a0and you should see something like this:\
\pard\pardeftab720\sl360\partightenfactor0
\ls1\ilvl0
\f1 \cf3 \cb4 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec3 ratings=# \\d\
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec3                 List of relations\
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec3  Schema |         Name          |   Type   |    Owner\
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec3 --------+-----------------------+----------+--------------\
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec3  public | users                 | table    | hackbright\
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec3  public | users_user_id_seq     | sequence | hackbright\
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec3 (2 rows)\
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec3 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec3 ratings=# \\d users\
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec3                                 Table "public.users"\
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec3   Column  |         Type          |                        Modifiers\
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec3 ----------+-----------------------+---------------------------------------------\
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec3  user_id  | integer               | not null default nextval ...\
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec3  email    | character varying(64) |\
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec3  password | character varying(64) |\
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec3  age      | integer               |\
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec3  zipcode  | character varying(15) |\
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec3 Indexes:\
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec3     "users_pkey" PRIMARY KEY, btree (user_id)\
\pard\tx220\tx720\pardeftab720\li720\fi-720\sl280\sa120\partightenfactor0
\ls1\ilvl0
\f0 \cf2 \cb1 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 \
\pard\pardeftab720\sl320\sa280\partightenfactor0

\b\fs28 \cf2 To Do\
\pard\pardeftab720\sl280\sa240\partightenfactor0

\b0\fs24 \cf2 Quit both\'a0
\i\b psql
\i0\b0 \'a0and\'a0
\i\b python
\i0\b0 .\
Drop your\'a0
\i\b ratings
\i0\b0 \'a0database (
\f2\fs28\fsmilli14400 \cf8 \strokec8 dropdb\'a0ratings
\f0\fs24 \cf2 \strokec2 ).\
Create two additional classes,\'a0
\i\b Movie
\i0\b0 \'a0and\'a0
\i\b Rating
\i0\b0 , to hold the information that we want to keep from those files (refer to the\'a0{\field{\*\fldinst{HYPERLINK "http://docs.sqlalchemy.org/en/latest/orm/tutorial.html"}}{\fldrslt \cf14 \strokec14 SQLAlchemy tutorial}}\'a0if necessary.)\
\pard\pardeftab720\sl280\sa240\partightenfactor0

\b \cf2 Movie
\b0 \

\itap1\trowd \taflags1 \trgaph108\trleft-108 \trbrdrt\brdrnil \trbrdrl\brdrnil \trbrdrr\brdrnil 
\clvertalb \clshdrawnil \clwWidth1254\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx4320
\clvertalb \clshdrawnil \clwWidth2452\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx8640
\pard\intbl\itap1\pardeftab720\sl280\qc\partightenfactor0

\b \cf2 Name\cell 
\pard\intbl\itap1\pardeftab720\sl280\qc\partightenfactor0
\cf2 Type\cell \row

\itap1\trowd \taflags1 \trgaph108\trleft-108 \trbrdrl\brdrnil \trbrdrr\brdrnil 
\clvertalt \clshdrawnil \clwWidth1254\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx4320
\clvertalt \clshdrawnil \clwWidth2452\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx8640
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0

\b0 \cf2 movie_id\cell 
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0
\cf2 integer, primary key\cell \row

\itap1\trowd \taflags1 \trgaph108\trleft-108 \trbrdrl\brdrnil \trbrdrr\brdrnil 
\clvertalt \clshdrawnil \clwWidth1254\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx4320
\clvertalt \clshdrawnil \clwWidth2452\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx8640
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0
\cf2 title\cell 
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0
\cf2 string\cell \row

\itap1\trowd \taflags1 \trgaph108\trleft-108 \trbrdrl\brdrnil \trbrdrr\brdrnil 
\clvertalt \clshdrawnil \clwWidth1254\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx4320
\clvertalt \clshdrawnil \clwWidth2452\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx8640
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0
\cf2 released_at\cell 
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0
\cf2 datetime\cell \row

\itap1\trowd \taflags1 \trgaph108\trleft-108 \trbrdrl\brdrnil \trbrdrb\brdrs\brdrw20\brdrcf7 \trbrdrr\brdrnil 
\clvertalt \clshdrawnil \clwWidth1254\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx4320
\clvertalt \clshdrawnil \clwWidth2452\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx8640
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0
\cf2 imdb_url\cell 
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0
\cf2 string\cell \lastrow\row
\pard\pardeftab720\sl280\sa240\partightenfactor0

\b \cf2 Rating
\b0 \

\itap1\trowd \taflags1 \trgaph108\trleft-108 \trbrdrt\brdrnil \trbrdrl\brdrnil \trbrdrr\brdrnil 
\clvertalb \clshdrawnil \clwWidth1061\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx4320
\clvertalb \clshdrawnil \clwWidth2094\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx8640
\pard\intbl\itap1\pardeftab720\sl280\qc\partightenfactor0

\b \cf2 Name\cell 
\pard\intbl\itap1\pardeftab720\sl280\qc\partightenfactor0
\cf2 Type\cell \row

\itap1\trowd \taflags1 \trgaph108\trleft-108 \trbrdrl\brdrnil \trbrdrr\brdrnil 
\clvertalt \clshdrawnil \clwWidth1061\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx4320
\clvertalt \clshdrawnil \clwWidth2094\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx8640
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0

\b0 \cf2 rating_id\cell 
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0
\cf2 integer, primary key\cell \row

\itap1\trowd \taflags1 \trgaph108\trleft-108 \trbrdrl\brdrnil \trbrdrr\brdrnil 
\clvertalt \clshdrawnil \clwWidth1061\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx4320
\clvertalt \clshdrawnil \clwWidth2094\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx8640
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0
\cf2 movie_id\cell 
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0
\cf2 integer\cell \row

\itap1\trowd \taflags1 \trgaph108\trleft-108 \trbrdrl\brdrnil \trbrdrr\brdrnil 
\clvertalt \clshdrawnil \clwWidth1061\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx4320
\clvertalt \clshdrawnil \clwWidth2094\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx8640
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0
\cf2 user_id\cell 
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0
\cf2 integer\cell \row

\itap1\trowd \taflags1 \trgaph108\trleft-108 \trbrdrl\brdrnil \trbrdrb\brdrs\brdrw20\brdrcf7 \trbrdrr\brdrnil 
\clvertalt \clshdrawnil \clwWidth1061\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx4320
\clvertalt \clshdrawnil \clwWidth2094\clftsWidth3 \clbrdrt\brdrs\brdrw20\brdrcf7 \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt72 \clpadl72 \clpadb72 \clpadr72 \gaph\cellx8640
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0
\cf2 score\cell 
\pard\intbl\itap1\pardeftab720\sl280\partightenfactor0
\cf2 integer\
\cell \lastrow\row
\pard\pardeftab720\sl320\sa280\partightenfactor0

\b\fs28 \cf2 Reading Data From Seed Files\
\pard\pardeftab720\sl280\sa240\partightenfactor0

\b0\fs24 \cf2 Now that we know how to insert single rows into the database, we have to\'a0
\i bulk insert
\i0 \'a0a bunch of our movie data. You\'92ll find a file,\'a0
\i\b seed.py
\i0\b0 , which contains a rough outline of what needs to happen. You\'92ll need to open up the seed files corresponding to each table, read each row in, parse it, then insert it into the database using our SQLAlchemy object interface.\
The general steps are:\
\pard\tx220\tx720\pardeftab720\li720\fi-720\sl280\partightenfactor0
\ls2\ilvl0\cf2 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	1.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Open and read a file\
\ls2\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	2.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Parse a line\
\ls2\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	3.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Create an object\
\ls2\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	4.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Add the object to the\'a0
\i\b db.session
\i0\b0 \
\ls2\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	5.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Repeat until all objects are added\
\ls2\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	6.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Commit\
\pard\pardeftab720\sl280\sa240\partightenfactor0
\cf2 We\'92ve supplied the first,\'a0
\f2\fs28\fsmilli14400 \cf8 \strokec8 load_users
\f0\fs24 \cf2 \strokec2 , to give you a sense of what to do for the others. Read it carefully. Each of the files is formatted slightly differently, so you\'92ll have to modify the second two functions to account for those changes.\
There are two particular challenges to pay attention to as you write your own\'a0
\f2\fs28\fsmilli14400 \cf8 \strokec8 load
\f0\fs24 \cf2 \strokec2 \'a0functions:\
\pard\tx220\tx720\pardeftab720\li720\fi-720\sl280\sa120\partightenfactor0
\ls3\ilvl0\cf2 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 In the\'a0
\i\b u.item
\i0\b0 \'a0file, the dates are given as strings like \'9331-Oct-2015\'94. We need to store this in the database as an actual date object, not as a string that just looks like a date. To do this, you\'92ll need to research the Python\'a0
\i\b datetime
\i0\b0 \'a0library to find the function that can parse a string into a datetime object.\
\ls3\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 The movies include the year of release at the end of the title, like \'93Balloonicorn\'92s Big Adventure (2010)\'94 \'96 but we don\'92t want to include that parenthetical date in the database (we\'92re already storing the release date as a separate field, so it\'92s duplicative, plus it\'92s ugly). Find a way to remove it from the title.\
\pard\pardeftab720\sl280\sa240\partightenfactor0
\cf2 Feeling stumped on your datetime conversion? Here\'92s a hint:\
Datetime Conversion\
You will need to use\'a0
\i\b strptime
\i0\b0 \'a0from the datetime library. Here\'92s some example code:\
\pard\pardeftab720\sl320\partightenfactor0

\f3\b\fs28\fsmilli14400 \cf10 \cb15 \strokec10 if
\f2\b0 \cf2 \strokec2  released_str:\
    released_at \cf12 \strokec12 =\cf2 \strokec2  datetime\cf12 \strokec12 .\cf2 \strokec2 datetime\cf12 \strokec12 .\cf2 \strokec2 strptime(released_str, \cf9 \strokec9 "
\f4\i \cf16 \strokec16 %d
\f2\i0 \cf9 \strokec9 -%b-%Y"\cf2 \strokec2 )\

\f3\b \cf10 \strokec10 else
\f2\b0 \cf2 \strokec2 :\
    released_at \cf12 \strokec12 =\cf2 \strokec2  
\f3\b \cf10 \strokec10 None
\f2\b0 \cf2 \cb1 \strokec2 \
}