# IBMassignment

+*In[1]:*+
[source, ipython3]
----
!pip install yfinance
!pip install bs4
!pip install nbformat
----


+*Out[1]:*+
----
Collecting yfinance
  Downloading yfinance-0.2.48-py2.py3-none-any.whl.metadata (13 kB)
Requirement already satisfied: pandas>=1.3.0 in /opt/conda/lib/python3.11/site-packages (from yfinance) (2.2.3)
Requirement already satisfied: numpy>=1.16.5 in /opt/conda/lib/python3.11/site-packages (from yfinance) (2.1.3)
Requirement already satisfied: requests>=2.31 in /opt/conda/lib/python3.11/site-packages (from yfinance) (2.31.0)
Collecting multitasking>=0.0.7 (from yfinance)
  Downloading multitasking-0.0.11-py3-none-any.whl.metadata (5.5 kB)
Requirement already satisfied: lxml>=4.9.1 in /opt/conda/lib/python3.11/site-packages (from yfinance) (5.3.0)
Requirement already satisfied: platformdirs>=2.0.0 in /opt/conda/lib/python3.11/site-packages (from yfinance) (4.2.1)
Requirement already satisfied: pytz>=2022.5 in /opt/conda/lib/python3.11/site-packages (from yfinance) (2024.1)
Collecting frozendict>=2.3.4 (from yfinance)
  Downloading frozendict-2.4.6-py311-none-any.whl.metadata (23 kB)
Collecting peewee>=3.16.2 (from yfinance)
  Downloading peewee-3.17.7.tar.gz (939 kB)
[2K     [90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━[0m [32m939.5/939.5 kB[0m [31m54.1 MB/s[0m eta [36m0:00:00[0m
[?25h  Installing build dependencies ... [?25ldone
[?25h  Getting requirements to build wheel ... [?25ldone
[?25h  Preparing metadata (pyproject.toml) ... [?25ldone
[?25hRequirement already satisfied: beautifulsoup4>=4.11.1 in /opt/conda/lib/python3.11/site-packages (from yfinance) (4.12.3)
Requirement already satisfied: html5lib>=1.1 in /opt/conda/lib/python3.11/site-packages (from yfinance) (1.1)
Requirement already satisfied: soupsieve>1.2 in /opt/conda/lib/python3.11/site-packages (from beautifulsoup4>=4.11.1->yfinance) (2.5)
Requirement already satisfied: six>=1.9 in /opt/conda/lib/python3.11/site-packages (from html5lib>=1.1->yfinance) (1.16.0)
Requirement already satisfied: webencodings in /opt/conda/lib/python3.11/site-packages (from html5lib>=1.1->yfinance) (0.5.1)
Requirement already satisfied: python-dateutil>=2.8.2 in /opt/conda/lib/python3.11/site-packages (from pandas>=1.3.0->yfinance) (2.9.0)
Requirement already satisfied: tzdata>=2022.7 in /opt/conda/lib/python3.11/site-packages (from pandas>=1.3.0->yfinance) (2024.2)
Requirement already satisfied: charset-normalizer<4,>=2 in /opt/conda/lib/python3.11/site-packages (from requests>=2.31->yfinance) (3.3.2)
Requirement already satisfied: idna<4,>=2.5 in /opt/conda/lib/python3.11/site-packages (from requests>=2.31->yfinance) (3.7)
Requirement already satisfied: urllib3<3,>=1.21.1 in /opt/conda/lib/python3.11/site-packages (from requests>=2.31->yfinance) (2.2.1)
Requirement already satisfied: certifi>=2017.4.17 in /opt/conda/lib/python3.11/site-packages (from requests>=2.31->yfinance) (2024.6.2)
Downloading yfinance-0.2.48-py2.py3-none-any.whl (101 kB)
[2K   [90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━[0m [32m101.1/101.1 kB[0m [31m7.7 MB/s[0m eta [36m0:00:00[0m
[?25hDownloading frozendict-2.4.6-py311-none-any.whl (16 kB)
Downloading multitasking-0.0.11-py3-none-any.whl (8.5 kB)
Building wheels for collected packages: peewee
  Building wheel for peewee (pyproject.toml) ... [?25ldone
[?25h  Created wheel for peewee: filename=peewee-3.17.7-py3-none-any.whl size=138905 sha256=5e84b8d774e2ce3eb063140af359aa1f638e0d1f66c50250166ef0bbc3031bbb
  Stored in directory: /home/jupyterlab/.cache/pip/wheels/fd/28/34/9ba1363b76703fe35ae8296af28ea74578a41b83544bb9da65
Successfully built peewee
Installing collected packages: peewee, multitasking, frozendict, yfinance
Successfully installed frozendict-2.4.6 multitasking-0.0.11 peewee-3.17.7 yfinance-0.2.48
Requirement already satisfied: bs4 in /opt/conda/lib/python3.11/site-packages (0.0.2)
Requirement already satisfied: beautifulsoup4 in /opt/conda/lib/python3.11/site-packages (from bs4) (4.12.3)
Requirement already satisfied: soupsieve>1.2 in /opt/conda/lib/python3.11/site-packages (from beautifulsoup4->bs4) (2.5)
Requirement already satisfied: nbformat in /opt/conda/lib/python3.11/site-packages (5.10.4)
Requirement already satisfied: fastjsonschema>=2.15 in /opt/conda/lib/python3.11/site-packages (from nbformat) (2.19.1)
Requirement already satisfied: jsonschema>=2.6 in /opt/conda/lib/python3.11/site-packages (from nbformat) (4.22.0)
Requirement already satisfied: jupyter-core!=5.0.*,>=4.12 in /opt/conda/lib/python3.11/site-packages (from nbformat) (5.7.2)
Requirement already satisfied: traitlets>=5.1 in /opt/conda/lib/python3.11/site-packages (from nbformat) (5.14.3)
Requirement already satisfied: attrs>=22.2.0 in /opt/conda/lib/python3.11/site-packages (from jsonschema>=2.6->nbformat) (23.2.0)
Requirement already satisfied: jsonschema-specifications>=2023.03.6 in /opt/conda/lib/python3.11/site-packages (from jsonschema>=2.6->nbformat) (2023.12.1)
Requirement already satisfied: referencing>=0.28.4 in /opt/conda/lib/python3.11/site-packages (from jsonschema>=2.6->nbformat) (0.35.1)
Requirement already satisfied: rpds-py>=0.7.1 in /opt/conda/lib/python3.11/site-packages (from jsonschema>=2.6->nbformat) (0.18.0)
Requirement already satisfied: platformdirs>=2.5 in /opt/conda/lib/python3.11/site-packages (from jupyter-core!=5.0.*,>=4.12->nbformat) (4.2.1)
----


+*In[2]:*+
[source, ipython3]
----
import yfinance as yf
import pandas as pd
import requests
from bs4 import BeautifulSoup
import plotly.graph_objects as go
from plotly.subplots import make_subplots
----




+*In[3]:*+
[source, ipython3]
----
import warnings
# Ignore all warnings
warnings.filterwarnings("ignore", category=FutureWarning)
----






+*In[41]:*+
[source, ipython3]
----
def make_graph(stock_data, revenue_data, stock):
    fig = make_subplots(rows=2, cols=1, shared_xaxes=True, subplot_titles=("Historical Share Price", "Historical Revenue"), vertical_spacing = .3)
    stock_data_specific = stock_data[stock_data.Date <= '2021-06-14']
    revenue_data_specific = revenue_data[revenue_data.Date <= '2021-04-30']
    fig.add_trace(go.Scatter(x=pd.to_datetime(stock_data_specific.Date, infer_datetime_format=True), y=stock_data_specific.Close.astype("string"), name="Share Price"), row=1, col=1)
    fig.add_trace(go.Scatter(x=pd.to_datetime(revenue_data_specific.Date, infer_datetime_format=True), y=revenue_data_specific.Revenue.astype("string"), name="Revenue"), row=2, col=1)
    fig.update_xaxes(title_text="Date", row=1, col=1)
    fig.update_xaxes(title_text="Date", row=2, col=1)
    fig.update_yaxes(title_text="Price ($US)", row=1, col=1)
    fig.update_yaxes(title_text="Revenue ($US Millions)", row=2, col=1)
    fig.update_layout(showlegend=False,
    height=900,
    title=stock,
    xaxis_rangeslider_visible=True)
    fig.show()
----








+*In[87]:*+
[source, ipython3]
----
tesla = yf.Ticker("TSLA")
----




+*In[88]:*+
[source, ipython3]
----
tesla_data = tesla.history(period="max")
----




+*In[89]:*+
[source, ipython3]
----
tesla_data.reset_index(inplace=True)
tesla_data.head()
----


+*Out[89]:*+
----
[cols=",,,,,,,,",options="header",]
|===
| |Date |Open |High |Low |Close |Volume |Dividends |Stock Splits
|0 |2010-06-29 00:00:00-04:00 |1.266667 |1.666667 |1.169333 |1.592667
|281494500 |0.0 |0.0

|1 |2010-06-30 00:00:00-04:00 |1.719333 |2.028000 |1.553333 |1.588667
|257806500 |0.0 |0.0

|2 |2010-07-01 00:00:00-04:00 |1.666667 |1.728000 |1.351333 |1.464000
|123282000 |0.0 |0.0

|3 |2010-07-02 00:00:00-04:00 |1.533333 |1.540000 |1.247333 |1.280000
|77097000 |0.0 |0.0

|4 |2010-07-06 00:00:00-04:00 |1.333333 |1.333333 |1.055333 |1.074000
|103003500 |0.0 |0.0
|===
----






+*In[91]:*+
[source, ipython3]
----
url = "https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0220EN-SkillsNetwork/labs/project/revenue.htm"
response = requests.get(url)
html_data = response.text
----




+*In[92]:*+
[source, ipython3]
----
from bs4 import BeautifulSoup
soup = BeautifulSoup(html_data, 'html.parser')
----








+*In[94]:*+
[source, ipython3]
----
tesla_revenue = pd.DataFrame(columns=['Date','Revenue'])
Revenue_Table=soup.find_all('table')
Table=Revenue_Table[1]

for row in Table.find('tbody').find_all('tr'):
    col=row.find_all('td')
    date=col[0].text
    revenue=col[1].text
    tesla_revenue=pd.concat([tesla_revenue,pd.DataFrame({'Date':[date],'Revenue':[revenue]})], ignore_index=True)
    tesla_revenue = tesla_revenue.sort_values('Date', ascending=True)
    tesla_revenue = tesla_revenue.reset_index(drop=True)

tesla_revenue
----


+*Out[94]:*+
----
[cols=",,",options="header",]
|===
| |Date |Revenue
|0 |2009-06-30 |$27
|1 |2009-09-30 |$46
|2 |2009-12-31 |
|3 |2010-03-31 |$21
|4 |2010-06-30 |$28
|5 |2010-09-30 |$31
|6 |2010-12-31 |$36
|7 |2011-03-31 |$49
|8 |2011-06-30 |$58
|9 |2011-09-30 |$58
|10 |2011-12-31 |$39
|11 |2012-03-31 |$30
|12 |2012-06-30 |$27
|13 |2012-09-30 |$50
|14 |2012-12-31 |$306
|15 |2013-03-31 |$562
|16 |2013-06-30 |$405
|17 |2013-09-30 |$431
|18 |2013-12-31 |$615
|19 |2014-03-31 |$621
|20 |2014-06-30 |$769
|21 |2014-09-30 |$852
|22 |2014-12-31 |$957
|23 |2015-03-31 |$940
|24 |2015-06-30 |$955
|25 |2015-09-30 |$937
|26 |2015-12-31 |$1,214
|27 |2016-03-31 |$1,147
|28 |2016-06-30 |$1,270
|29 |2016-09-30 |$2,298
|30 |2016-12-31 |$2,285
|31 |2017-03-31 |$2,696
|32 |2017-06-30 |$2,790
|33 |2017-09-30 |$2,985
|34 |2017-12-31 |$3,288
|35 |2018-03-31 |$3,409
|36 |2018-06-30 |$4,002
|37 |2018-09-30 |$6,824
|38 |2018-12-31 |$7,226
|39 |2019-03-31 |$4,541
|40 |2019-06-30 |$6,350
|41 |2019-09-30 |$6,303
|42 |2019-12-31 |$7,384
|43 |2020-03-31 |$5,985
|44 |2020-06-30 |$6,036
|45 |2020-09-30 |$8,771
|46 |2020-12-31 |$10,744
|47 |2021-03-31 |$10,389
|48 |2021-06-30 |$11,958
|49 |2021-09-30 |$13,757
|50 |2021-12-31 |$17,719
|51 |2022-03-31 |$18,756
|52 |2022-06-30 |$16,934
|53 |2022-09-30 |$21,454
|===
----




+*In[95]:*+
[source, ipython3]
----
tesla_revenue["Revenue"] = tesla_revenue['Revenue'].str.replace(',|\$',"")
----




+*In[96]:*+
[source, ipython3]
----
tesla_revenue.dropna(inplace=True)

tesla_revenue = tesla_revenue[tesla_revenue['Revenue'] != ""]
----




+*In[97]:*+
[source, ipython3]
----
tesla_revenue.tail()
----


+*Out[97]:*+
----
[cols=",,",options="header",]
|===
| |Date |Revenue
|49 |2021-09-30 |$13,757
|50 |2021-12-31 |$17,719
|51 |2022-03-31 |$18,756
|52 |2022-06-30 |$16,934
|53 |2022-09-30 |$21,454
|===
----






+*In[98]:*+
[source, ipython3]
----
gamestop = yf.Ticker("GME")
----




+*In[99]:*+
[source, ipython3]
----
gme_data = gamestop.history(period="max")
----




+*In[100]:*+
[source, ipython3]
----
gme_data.reset_index(inplace=True)
gme_data.head()
----


+*Out[100]:*+
----
[cols=",,,,,,,,",options="header",]
|===
| |Date |Open |High |Low |Close |Volume |Dividends |Stock Splits
|0 |2002-02-13 00:00:00-05:00 |1.620128 |1.693350 |1.603296 |1.691666
|76216000 |0.0 |0.0

|1 |2002-02-14 00:00:00-05:00 |1.712707 |1.716074 |1.670626 |1.683250
|11021600 |0.0 |0.0

|2 |2002-02-15 00:00:00-05:00 |1.683250 |1.687458 |1.658002 |1.674834
|8389600 |0.0 |0.0

|3 |2002-02-19 00:00:00-05:00 |1.666417 |1.666417 |1.578047 |1.607504
|7410400 |0.0 |0.0

|4 |2002-02-20 00:00:00-05:00 |1.615921 |1.662210 |1.603296 |1.662210
|6892800 |0.0 |0.0
|===
----






+*In[121]:*+
[source, ipython3]
----
url_2="https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0220EN-SkillsNetwork/labs/project/stock.html"
response_2 = requests.get(url_2)
html_data_2 = response_2.text
----




+*In[122]:*+
[source, ipython3]
----
soup_2=BeautifulSoup(html_data_2,'html.parser')
----








+*In[123]:*+
[source, ipython3]
----
gme_revenue = pd.DataFrame(columns=['Date','Revenue'])
Revenue_Table_2=soup_2.find_all('table')
Table_2=Revenue_Table_2[1]

for row_2 in Table_2.find('tbody').find_all('tr'):
    col_2=row_2.find_all('td')
    date_2=col_2[0].text
    revenue_2=col_2[1].text
    gme_revenue=pd.concat([gme_revenue,pd.DataFrame({'Date':[date_2],'Revenue':[revenue_2]})], ignore_index=True)
    gme_revenue = gme_revenue.sort_values('Date', ascending=True)
    gme_revenue = gme_revenue.reset_index(drop=True)

gme_revenue
----


+*Out[123]:*+
----
[cols=",,",options="header",]
|===
| |Date |Revenue
|0 |2005-01-31 |$709
|1 |2005-04-30 |$475
|2 |2005-07-31 |$416
|3 |2005-10-31 |$534
|4 |2006-01-31 |$1,667
|... |... |...
|57 |2019-04-30 |$1,548
|58 |2019-07-31 |$1,286
|59 |2019-10-31 |$1,439
|60 |2020-01-31 |$2,194
|61 |2020-04-30 |$1,021
|===

62 rows × 2 columns
----




+*In[124]:*+
[source, ipython3]
----
gme_revenue.tail()
----


+*Out[124]:*+
----
[cols=",,",options="header",]
|===
| |Date |Revenue
|57 |2019-04-30 |$1,548
|58 |2019-07-31 |$1,286
|59 |2019-10-31 |$1,439
|60 |2020-01-31 |$2,194
|61 |2020-04-30 |$1,021
|===
----








+*In[112]:*+
[source, ipython3]
----
make_graph(tesla_data, tesla_revenue, 'Tesla')
----


+*Out[112]:*+
----
/tmp/ipykernel_649/1275048830.py:5: UserWarning:

The argument 'infer_datetime_format' is deprecated and will be removed in a future version. A strict version of it is now the default, see https://pandas.pydata.org/pdeps/0004-consistent-to-datetime-parsing.html. You can safely remove this argument.

/tmp/ipykernel_649/1275048830.py:6: UserWarning:

The argument 'infer_datetime_format' is deprecated and will be removed in a future version. A strict version of it is now the default, see https://pandas.pydata.org/pdeps/0004-consistent-to-datetime-parsing.html. You can safely remove this argument.


[[3c9a0123-c9cc-4e39-b2d4-7933c18f0b98]]
----








+*In[125]:*+
[source, ipython3]
----
make_graph(gme_data, gme_revenue, 'GameStop')
----


+*Out[125]:*+
----
/tmp/ipykernel_649/1275048830.py:5: UserWarning:

The argument 'infer_datetime_format' is deprecated and will be removed in a future version. A strict version of it is now the default, see https://pandas.pydata.org/pdeps/0004-consistent-to-datetime-parsing.html. You can safely remove this argument.

/tmp/ipykernel_649/1275048830.py:6: UserWarning:

The argument 'infer_datetime_format' is deprecated and will be removed in a future version. A strict version of it is now the default, see https://pandas.pydata.org/pdeps/0004-consistent-to-datetime-parsing.html. You can safely remove this argument.


[[78b573d1-a5b7-4c82-bef1-c2a92ddb2c85]]
----
