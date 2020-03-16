

```python
import pandas as pd
link= "https://docs.google.com/spreadsheets/d/e/2PACX-1vRwqjWnJJZIyrDToBjeao-xiXBrDcmCtAO5tG5Nk0OORLF-KBN4JSL81XXoDbF9-Uf_ZY0pOH-akaNu/pub?gid=587720900&single=true&output=csv"
internet=pd.read_csv(link)
```


```python
internet
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Country or Area</th>
      <th>Year</th>
      <th>Value</th>
      <th>Value Footnotes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Albania</td>
      <td>2000</td>
      <td>0.114097</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Algeria</td>
      <td>2000</td>
      <td>0.491706</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Andorra</td>
      <td>2000</td>
      <td>10.538836</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Angola</td>
      <td>2000</td>
      <td>0.105046</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Antigua and Barbuda</td>
      <td>2000</td>
      <td>6.482226</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>217</th>
      <td>17</td>
      <td>November. Population age 14+.</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>218</th>
      <td>18</td>
      <td>Estimation based on GPRS subscribers, fixed an...</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>219</th>
      <td>19</td>
      <td>In the last 6 months. Population age 14+</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>220</th>
      <td>20</td>
      <td>Population age 16-74.</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>221</th>
      <td>21</td>
      <td>Population age 16+ using internet in the last ...</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
<p>222 rows × 4 columns</p>
</div>




```python
internet.drop(columns='Value Footnotes')
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Country or Area</th>
      <th>Year</th>
      <th>Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Albania</td>
      <td>2000</td>
      <td>0.114097</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Algeria</td>
      <td>2000</td>
      <td>0.491706</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Andorra</td>
      <td>2000</td>
      <td>10.538836</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Angola</td>
      <td>2000</td>
      <td>0.105046</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Antigua and Barbuda</td>
      <td>2000</td>
      <td>6.482226</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>217</th>
      <td>17</td>
      <td>November. Population age 14+.</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>218</th>
      <td>18</td>
      <td>Estimation based on GPRS subscribers, fixed an...</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>219</th>
      <td>19</td>
      <td>In the last 6 months. Population age 14+</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>220</th>
      <td>20</td>
      <td>Population age 16-74.</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>221</th>
      <td>21</td>
      <td>Population age 16+ using internet in the last ...</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
<p>222 rows × 3 columns</p>
</div>




```python
internet.drop(columns = 'Year')
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Country or Area</th>
      <th>Value</th>
      <th>Value Footnotes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Albania</td>
      <td>0.114097</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Algeria</td>
      <td>0.491706</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Andorra</td>
      <td>10.538836</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Angola</td>
      <td>0.105046</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Antigua and Barbuda</td>
      <td>6.482226</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>217</th>
      <td>17</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>218</th>
      <td>18</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>219</th>
      <td>19</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>220</th>
      <td>20</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>221</th>
      <td>21</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
<p>222 rows × 3 columns</p>
</div>




```python
internet.drop(columns='Value Footnotes', inplace=True)
```


```python
internet.drop(columns= 'Year', inplace=True)
```


```python
internet.reset_index(drop=True, inplace=True)
```


```python
internet.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Country or Area</th>
      <th>Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Albania</td>
      <td>0.114097</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Algeria</td>
      <td>0.491706</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Andorra</td>
      <td>10.538836</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Angola</td>
      <td>0.105046</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Antigua and Barbuda</td>
      <td>6.482226</td>
    </tr>
  </tbody>
</table>
</div>




```python
OldToNew={internet.columns[0]:'Country', internet.columns[1]:'Usage'}
```


```python
OldToNew
```




    {'Country or Area': 'Country', 'Value': 'Usage'}




```python
internet.rename(columns=OldToNew)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Country</th>
      <th>Usage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Albania</td>
      <td>0.114097</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Algeria</td>
      <td>0.491706</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Andorra</td>
      <td>10.538836</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Angola</td>
      <td>0.105046</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Antigua and Barbuda</td>
      <td>6.482226</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>217</th>
      <td>17</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>218</th>
      <td>18</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>219</th>
      <td>19</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>220</th>
      <td>20</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>221</th>
      <td>21</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
<p>222 rows × 2 columns</p>
</div>




```python
internet.rename(columns=OldToNew,inplace=True)
```


```python
internet.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Country</th>
      <th>Usage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Albania</td>
      <td>0.114097</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Algeria</td>
      <td>0.491706</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Andorra</td>
      <td>10.538836</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Angola</td>
      <td>0.105046</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Antigua and Barbuda</td>
      <td>6.482226</td>
    </tr>
  </tbody>
</table>
</div>




```python
internet.Country.unique().tolist()
```




    ['Albania',
     'Algeria',
     'Andorra',
     'Angola',
     'Antigua and Barbuda',
     'Argentina',
     'Armenia',
     'Aruba',
     'Australia',
     'Austria',
     'Azerbaijan',
     'Bahamas',
     'Bahrain',
     'Bangladesh',
     'Barbados',
     'Belarus',
     'Belgium',
     'Belize',
     'Benin',
     'Bermuda',
     'Bhutan',
     'Bolivia',
     'Bosnia and Herzegovina',
     'Botswana',
     'Brazil',
     'Brunei Darussalam',
     'Bulgaria',
     'Burkina Faso',
     'Burundi',
     'Cambodia',
     'Cameroon',
     'Canada',
     'Cape Verde',
     'Central African Rep.',
     'Chad',
     'Chile',
     'China',
     'Colombia',
     'Comoros',
     'Congo',
     'Congo (Democratic Republic of the)',
     'Costa Rica',
     "Cote d'Ivoire",
     'Croatia',
     'Cuba',
     'Cyprus',
     'Czech Republic',
     "Dem. People's Rep. of Korea",
     'Denmark',
     'Djibouti',
     'Dominica',
     'Dominican Rep.',
     'Ecuador',
     'Egypt',
     'El Salvador',
     'Equatorial Guinea',
     'Eritrea',
     'Estonia',
     'Ethiopia',
     'Faroe Islands',
     'Fiji',
     'Finland',
     'France',
     'French Guiana',
     'French Polynesia',
     'Gabon',
     'Gambia',
     'Georgia',
     'Germany',
     'Ghana',
     'Gibraltar',
     'Greece',
     'Greenland',
     'Grenada',
     'Guam',
     'Guatemala',
     'Guernsey',
     'Guinea',
     'Guinea-Bissau',
     'Guyana',
     'Haiti',
     'Honduras',
     'Hong Kong, China',
     'Hungary',
     'Iceland',
     'India',
     'Indonesia',
     'Iran (Islamic Rep. of)',
     'Ireland',
     'Israel',
     'Italy',
     'Jamaica',
     'Japan',
     'Jersey',
     'Jordan',
     'Kazakhstan',
     'Kenya',
     'Kiribati',
     'Korea (Rep. of)',
     'Kuwait',
     'Kyrgyzstan',
     'Lao P.D.R.',
     'Latvia',
     'Lebanon',
     'Lesotho',
     'Liberia',
     'Libya',
     'Liechtenstein',
     'Lithuania',
     'Luxembourg',
     'Macao, China',
     'Madagascar',
     'Malawi',
     'Malaysia',
     'Maldives',
     'Mali',
     'Malta',
     'Marshall Islands',
     'Mauritania',
     'Mauritius',
     'Mexico',
     'Micronesia (Fed. States of)',
     'Moldova',
     'Monaco',
     'Mongolia',
     'Morocco',
     'Mozambique',
     'Namibia',
     'Nepal',
     'Netherlands',
     'New Caledonia',
     'New Zealand',
     'Nicaragua',
     'Niger',
     'Nigeria',
     'Norway',
     'Oman',
     'Palestine',
     'Panama',
     'Papua New Guinea',
     'Paraguay',
     'Peru',
     'Philippines',
     'Poland',
     'Portugal',
     'Puerto Rico',
     'Qatar',
     'Romania',
     'Russia',
     'Rwanda',
     'Saint Kitts and Nevis',
     'Saint Lucia',
     'Samoa',
     'San Marino',
     'Sao Tome and Principe',
     'Saudi Arabia',
     'Senegal',
     'Seychelles',
     'Sierra Leone',
     'Singapore',
     'Slovak Republic',
     'Slovenia',
     'Solomon Islands',
     'Somalia',
     'South Africa',
     'Spain',
     'Sri Lanka',
     'St. Vincent and the Grenadines',
     'Sudan',
     'Suriname',
     'Swaziland',
     'Sweden',
     'Switzerland',
     'Syria',
     'T.F.Y.R. Macedonia',
     'Tajikistan',
     'Tanzania',
     'Thailand',
     'Togo',
     'Tonga',
     'Trinidad and Tobago',
     'Tunisia',
     'Turkey',
     'Turkmenistan',
     'Tuvalu',
     'Uganda',
     'Ukraine',
     'United Arab Emirates',
     'United Kingdom',
     'United States',
     'Uruguay',
     'Uzbekistan',
     'Vanuatu',
     'Venezuela',
     'Viet Nam',
     'Virgin Islands (U.S.)',
     'Yemen',
     'Zambia',
     'Zimbabwe',
     nan,
     'footnoteSeqID',
     '1',
     '2',
     '3',
     '4',
     '5',
     '6',
     '7',
     '8',
     '9',
     '10',
     '11',
     '12',
     '13',
     '14',
     '15',
     '16',
     '17',
     '18',
     '19',
     '20',
     '21']




```python
#internet.Year.unique().tolist()
```


```python
internet.tail(20)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Country</th>
      <th>Usage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>202</th>
      <td>2</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>203</th>
      <td>3</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>204</th>
      <td>4</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>205</th>
      <td>5</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>206</th>
      <td>6</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>207</th>
      <td>7</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>208</th>
      <td>8</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>209</th>
      <td>9</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>210</th>
      <td>10</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>211</th>
      <td>11</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>212</th>
      <td>12</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>213</th>
      <td>13</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>214</th>
      <td>14</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>215</th>
      <td>15</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>216</th>
      <td>16</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>217</th>
      <td>17</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>218</th>
      <td>18</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>219</th>
      <td>19</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>220</th>
      <td>20</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>221</th>
      <td>21</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
#row 201 is last row with data

internet.drop(index=range(199,222))
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Country</th>
      <th>Usage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Albania</td>
      <td>0.114097</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Algeria</td>
      <td>0.491706</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Andorra</td>
      <td>10.538836</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Angola</td>
      <td>0.105046</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Antigua and Barbuda</td>
      <td>6.482226</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>194</th>
      <td>Viet Nam</td>
      <td>0.254248</td>
    </tr>
    <tr>
      <th>195</th>
      <td>Virgin Islands (U.S.)</td>
      <td>13.815081</td>
    </tr>
    <tr>
      <th>196</th>
      <td>Yemen</td>
      <td>0.082500</td>
    </tr>
    <tr>
      <th>197</th>
      <td>Zambia</td>
      <td>0.191072</td>
    </tr>
    <tr>
      <th>198</th>
      <td>Zimbabwe</td>
      <td>0.401434</td>
    </tr>
  </tbody>
</table>
<p>199 rows × 2 columns</p>
</div>




```python
internet.drop(index=range(199,222), inplace =True)
```


```python
internet
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Country</th>
      <th>Usage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Albania</td>
      <td>0.114097</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Algeria</td>
      <td>0.491706</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Andorra</td>
      <td>10.538836</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Angola</td>
      <td>0.105046</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Antigua and Barbuda</td>
      <td>6.482226</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>194</th>
      <td>Viet Nam</td>
      <td>0.254248</td>
    </tr>
    <tr>
      <th>195</th>
      <td>Virgin Islands (U.S.)</td>
      <td>13.815081</td>
    </tr>
    <tr>
      <th>196</th>
      <td>Yemen</td>
      <td>0.082500</td>
    </tr>
    <tr>
      <th>197</th>
      <td>Zambia</td>
      <td>0.191072</td>
    </tr>
    <tr>
      <th>198</th>
      <td>Zimbabwe</td>
      <td>0.401434</td>
    </tr>
  </tbody>
</table>
<p>199 rows × 2 columns</p>
</div>




```python
#internet.Year.unique().tolist()
```


```python
internet.info()
```

    <class 'pandas.core.frame.DataFrame'>
    Int64Index: 199 entries, 0 to 198
    Data columns (total 2 columns):
    Country    199 non-null object
    Usage      199 non-null float64
    dtypes: float64(1), object(1)
    memory usage: 4.7+ KB
    


```python
#pd.to_numeric(internet.Year)
```


```python
#internet = internet.assign(Year = pd.to_numeric(internet.Year))
```


```python
internet.dtypes
```




    Country     object
    Usage      float64
    dtype: object



Merging with Mortality Data


```python
from urllib.request import urlopen
mort = pd.read_pickle(urlopen('https://github.com/sleouw/542data/raw/master/UNmortality4.pkl'),compression=None)
```


```python
mort
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Country</th>
      <th>Gender</th>
      <th>Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Afghanistan</td>
      <td>Female</td>
      <td>301</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Albania</td>
      <td>Female</td>
      <td>103</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Algeria</td>
      <td>Female</td>
      <td>138</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Andorra</td>
      <td>Female</td>
      <td>50</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Angola</td>
      <td>Female</td>
      <td>390</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>189</th>
      <td>Venezuela (Bolivarian Republic of)</td>
      <td>Female</td>
      <td>98</td>
    </tr>
    <tr>
      <th>190</th>
      <td>Viet Nam</td>
      <td>Female</td>
      <td>79</td>
    </tr>
    <tr>
      <th>191</th>
      <td>Yemen</td>
      <td>Female</td>
      <td>230</td>
    </tr>
    <tr>
      <th>192</th>
      <td>Zambia</td>
      <td>Female</td>
      <td>633</td>
    </tr>
    <tr>
      <th>193</th>
      <td>Zimbabwe</td>
      <td>Female</td>
      <td>764</td>
    </tr>
  </tbody>
</table>
<p>194 rows × 3 columns</p>
</div>




```python
intermort_dirty = internet.merge(mort,how='outer',indicator=True)
```


```python
intermort_dirty
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Country</th>
      <th>Usage</th>
      <th>Gender</th>
      <th>Value</th>
      <th>_merge</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Albania</td>
      <td>0.114097</td>
      <td>Female</td>
      <td>103.0</td>
      <td>both</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Algeria</td>
      <td>0.491706</td>
      <td>Female</td>
      <td>138.0</td>
      <td>both</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Andorra</td>
      <td>10.538836</td>
      <td>Female</td>
      <td>50.0</td>
      <td>both</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Angola</td>
      <td>0.105046</td>
      <td>Female</td>
      <td>390.0</td>
      <td>both</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Antigua and Barbuda</td>
      <td>6.482226</td>
      <td>Female</td>
      <td>148.0</td>
      <td>both</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>226</th>
      <td>The former Yugoslav Republic of Macedonia</td>
      <td>NaN</td>
      <td>Female</td>
      <td>87.0</td>
      <td>right_only</td>
    </tr>
    <tr>
      <th>227</th>
      <td>Timor-Leste</td>
      <td>NaN</td>
      <td>Female</td>
      <td>253.0</td>
      <td>right_only</td>
    </tr>
    <tr>
      <th>228</th>
      <td>United Republic of Tanzania</td>
      <td>NaN</td>
      <td>Female</td>
      <td>427.0</td>
      <td>right_only</td>
    </tr>
    <tr>
      <th>229</th>
      <td>United States of America</td>
      <td>NaN</td>
      <td>Female</td>
      <td>83.0</td>
      <td>right_only</td>
    </tr>
    <tr>
      <th>230</th>
      <td>Venezuela (Bolivarian Republic of)</td>
      <td>NaN</td>
      <td>Female</td>
      <td>98.0</td>
      <td>right_only</td>
    </tr>
  </tbody>
</table>
<p>231 rows × 5 columns</p>
</div>




```python
#request countries where demodex data found no match
intermort_dirty.loc[intermort_dirty['_merge']=='right_only', "Country"]
```




    199                                  Afghanistan
    200             Bolivia (Plurinational State of)
    201                                   Cabo Verde
    202                     Central African Republic
    203                                 Cook Islands
    204                                Côte d’Ivoire
    205        Democratic People's Republic of Korea
    206             Democratic Republic of the Congo
    207                           Dominican Republic
    208                   Iran (Islamic Republic of)
    209                                         Iraq
    210             Lao People's Democratic Republic
    211             Micronesia (Federated States of)
    212                                   Montenegro
    213                                      Myanmar
    214                                        Nauru
    215                                         Niue
    216                                     Pakistan
    217                                        Palau
    218                            Republic of Korea
    219                          Republic of Moldova
    220                           Russian Federation
    221             Saint Vincent and the Grenadines
    222                                       Serbia
    223                                     Slovakia
    224                                  South Sudan
    225                         Syrian Arab Republic
    226    The former Yugoslav Republic of Macedonia
    227                                  Timor-Leste
    228                  United Republic of Tanzania
    229                     United States of America
    230           Venezuela (Bolivarian Republic of)
    Name: Country, dtype: object




```python
#Look where hdi data frame found no match
intermort_dirty.loc[intermort_dirty['_merge']=='left_only',"Country"]
```




    7                                   Aruba
    19                                Bermuda
    21                                Bolivia
    32                             Cape Verde
    33                   Central African Rep.
    40     Congo (Democratic Republic of the)
    42                          Cote d'Ivoire
    47            Dem. People's Rep. of Korea
    51                         Dominican Rep.
    59                          Faroe Islands
    63                          French Guiana
    64                       French Polynesia
    70                              Gibraltar
    72                              Greenland
    74                                   Guam
    76                               Guernsey
    82                       Hong Kong, China
    87                 Iran (Islamic Rep. of)
    93                                 Jersey
    98                        Korea (Rep. of)
    101                            Lao P.D.R.
    107                         Liechtenstein
    110                          Macao, China
    121           Micronesia (Fed. States of)
    122                               Moldova
    130                         New Caledonia
    137                             Palestine
    145                           Puerto Rico
    148                                Russia
    160                       Slovak Republic
    167        St. Vincent and the Grenadines
    173                                 Syria
    174                    T.F.Y.R. Macedonia
    176                              Tanzania
    189                         United States
    193                             Venezuela
    195                 Virgin Islands (U.S.)
    Name: Country, dtype: object




```python
replacements1 = {'Bolivia (Plurinational State of)':'Bolivia','Cabo Verde':'Cape Verde','Central Africa Republic':'Central Africa Rep.','Democratic Republic of the Congo':'Congo (Democratic Republic of the)','Côte d’Ivoire':"Cote d'Ivoire","Democratic People's Republic of Korea":"Dem. People's Rep. of Korea",'Dominican Republic':'Dominican Rep.','Iran (Islamic Republic of)':'Iran (Islamic Rep. of)',"Lao People's Democratic Republic":"Lao P.D.R.","Micronesia(Federated States of)":"Micronesia(Fed. States of)","Republic of Moldova":"Moldova","Russian Federation":"Russia","Saint Vincent and the Grenadines":"St. Vincent and the Grenadines","Syrian Arab Republic":"Syria","The former Yugoslav Republic of Macedonia":"T.F.Y.R. Macedonia","United Republic of Tanzania":"Tanzania","United States of America":"United States","Venezuela (Bolivarian Republic of)":"Venezuela"}
```


```python
replacements1
```




    {'Bolivia (Plurinational State of)': 'Bolivia',
     'Cabo Verde': 'Cape Verde',
     'Central Africa Republic': 'Central Africa Rep.',
     'Democratic Republic of the Congo': 'Congo (Democratic Republic of the)',
     'Côte d’Ivoire': "Cote d'Ivoire",
     "Democratic People's Republic of Korea": "Dem. People's Rep. of Korea",
     'Dominican Republic': 'Dominican Rep.',
     'Iran (Islamic Republic of)': 'Iran (Islamic Rep. of)',
     "Lao People's Democratic Republic": 'Lao P.D.R.',
     'Micronesia(Federated States of)': 'Micronesia(Fed. States of)',
     'Republic of Moldova': 'Moldova',
     'Russian Federation': 'Russia',
     'Saint Vincent and the Grenadines': 'St. Vincent and the Grenadines',
     'Syrian Arab Republic': 'Syria',
     'The former Yugoslav Republic of Macedonia': 'T.F.Y.R. Macedonia',
     'United Republic of Tanzania': 'Tanzania',
     'United States of America': 'United States',
     'Venezuela (Bolivarian Republic of)': 'Venezuela'}




```python
# replacing
mort.Country.replace(replacements1,inplace=True)
                     
mort.tail(20)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Country</th>
      <th>Gender</th>
      <th>Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>174</th>
      <td>Tonga</td>
      <td>Female</td>
      <td>188</td>
    </tr>
    <tr>
      <th>175</th>
      <td>Trinidad and Tobago</td>
      <td>Female</td>
      <td>144</td>
    </tr>
    <tr>
      <th>176</th>
      <td>Tunisia</td>
      <td>Female</td>
      <td>89</td>
    </tr>
    <tr>
      <th>177</th>
      <td>Turkey</td>
      <td>Female</td>
      <td>103</td>
    </tr>
    <tr>
      <th>178</th>
      <td>Turkmenistan</td>
      <td>Female</td>
      <td>204</td>
    </tr>
    <tr>
      <th>179</th>
      <td>Tuvalu</td>
      <td>Female</td>
      <td>231</td>
    </tr>
    <tr>
      <th>180</th>
      <td>Uganda</td>
      <td>Female</td>
      <td>559</td>
    </tr>
    <tr>
      <th>181</th>
      <td>Ukraine</td>
      <td>Female</td>
      <td>136</td>
    </tr>
    <tr>
      <th>182</th>
      <td>United Arab Emirates</td>
      <td>Female</td>
      <td>89</td>
    </tr>
    <tr>
      <th>183</th>
      <td>United Kingdom</td>
      <td>Female</td>
      <td>67</td>
    </tr>
    <tr>
      <th>184</th>
      <td>Tanzania</td>
      <td>Female</td>
      <td>427</td>
    </tr>
    <tr>
      <th>185</th>
      <td>United States</td>
      <td>Female</td>
      <td>83</td>
    </tr>
    <tr>
      <th>186</th>
      <td>Uruguay</td>
      <td>Female</td>
      <td>90</td>
    </tr>
    <tr>
      <th>187</th>
      <td>Uzbekistan</td>
      <td>Female</td>
      <td>151</td>
    </tr>
    <tr>
      <th>188</th>
      <td>Vanuatu</td>
      <td>Female</td>
      <td>162</td>
    </tr>
    <tr>
      <th>189</th>
      <td>Venezuela</td>
      <td>Female</td>
      <td>98</td>
    </tr>
    <tr>
      <th>190</th>
      <td>Viet Nam</td>
      <td>Female</td>
      <td>79</td>
    </tr>
    <tr>
      <th>191</th>
      <td>Yemen</td>
      <td>Female</td>
      <td>230</td>
    </tr>
    <tr>
      <th>192</th>
      <td>Zambia</td>
      <td>Female</td>
      <td>633</td>
    </tr>
    <tr>
      <th>193</th>
      <td>Zimbabwe</td>
      <td>Female</td>
      <td>764</td>
    </tr>
  </tbody>
</table>
</div>




```python
intermort=internet.merge(mort)

```


```python
intermort.tail(25)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Country</th>
      <th>Usage</th>
      <th>Gender</th>
      <th>Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>153</th>
      <td>Syria</td>
      <td>0.181699</td>
      <td>Female</td>
      <td>102</td>
    </tr>
    <tr>
      <th>154</th>
      <td>T.F.Y.R. Macedonia</td>
      <td>2.485566</td>
      <td>Female</td>
      <td>87</td>
    </tr>
    <tr>
      <th>155</th>
      <td>Tajikistan</td>
      <td>0.048600</td>
      <td>Female</td>
      <td>178</td>
    </tr>
    <tr>
      <th>156</th>
      <td>Tanzania</td>
      <td>0.117194</td>
      <td>Female</td>
      <td>427</td>
    </tr>
    <tr>
      <th>157</th>
      <td>Thailand</td>
      <td>3.689041</td>
      <td>Female</td>
      <td>126</td>
    </tr>
    <tr>
      <th>158</th>
      <td>Togo</td>
      <td>0.800000</td>
      <td>Female</td>
      <td>333</td>
    </tr>
    <tr>
      <th>159</th>
      <td>Tonga</td>
      <td>2.434398</td>
      <td>Female</td>
      <td>188</td>
    </tr>
    <tr>
      <th>160</th>
      <td>Trinidad and Tobago</td>
      <td>7.721411</td>
      <td>Female</td>
      <td>144</td>
    </tr>
    <tr>
      <th>161</th>
      <td>Tunisia</td>
      <td>2.750740</td>
      <td>Female</td>
      <td>89</td>
    </tr>
    <tr>
      <th>162</th>
      <td>Turkey</td>
      <td>3.761685</td>
      <td>Female</td>
      <td>103</td>
    </tr>
    <tr>
      <th>163</th>
      <td>Turkmenistan</td>
      <td>0.133282</td>
      <td>Female</td>
      <td>204</td>
    </tr>
    <tr>
      <th>164</th>
      <td>Tuvalu</td>
      <td>5.241640</td>
      <td>Female</td>
      <td>231</td>
    </tr>
    <tr>
      <th>165</th>
      <td>Uganda</td>
      <td>0.163714</td>
      <td>Female</td>
      <td>559</td>
    </tr>
    <tr>
      <th>166</th>
      <td>Ukraine</td>
      <td>0.716184</td>
      <td>Female</td>
      <td>136</td>
    </tr>
    <tr>
      <th>167</th>
      <td>United Arab Emirates</td>
      <td>23.625301</td>
      <td>Female</td>
      <td>89</td>
    </tr>
    <tr>
      <th>168</th>
      <td>United Kingdom</td>
      <td>26.821754</td>
      <td>Female</td>
      <td>67</td>
    </tr>
    <tr>
      <th>169</th>
      <td>United States</td>
      <td>43.079163</td>
      <td>Female</td>
      <td>83</td>
    </tr>
    <tr>
      <th>170</th>
      <td>Uruguay</td>
      <td>10.539058</td>
      <td>Female</td>
      <td>90</td>
    </tr>
    <tr>
      <th>171</th>
      <td>Uzbekistan</td>
      <td>0.484347</td>
      <td>Female</td>
      <td>151</td>
    </tr>
    <tr>
      <th>172</th>
      <td>Vanuatu</td>
      <td>2.108337</td>
      <td>Female</td>
      <td>162</td>
    </tr>
    <tr>
      <th>173</th>
      <td>Venezuela</td>
      <td>3.359597</td>
      <td>Female</td>
      <td>98</td>
    </tr>
    <tr>
      <th>174</th>
      <td>Viet Nam</td>
      <td>0.254248</td>
      <td>Female</td>
      <td>79</td>
    </tr>
    <tr>
      <th>175</th>
      <td>Yemen</td>
      <td>0.082500</td>
      <td>Female</td>
      <td>230</td>
    </tr>
    <tr>
      <th>176</th>
      <td>Zambia</td>
      <td>0.191072</td>
      <td>Female</td>
      <td>633</td>
    </tr>
    <tr>
      <th>177</th>
      <td>Zimbabwe</td>
      <td>0.401434</td>
      <td>Female</td>
      <td>764</td>
    </tr>
  </tbody>
</table>
</div>




```python
fert = pd.read_pickle(urlopen('https://github.com/aaront002/Marriage-and-Ed/raw/master/contmared.pkl'),compression=None)
```


```python
fert
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>ContinentCode</th>
      <th>CountryCode</th>
      <th>CountryName</th>
      <th>FertilityRate</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>AS</td>
      <td>AFG</td>
      <td>Afghanistan</td>
      <td>7.485</td>
    </tr>
    <tr>
      <th>1</th>
      <td>EU</td>
      <td>ALB</td>
      <td>Albania</td>
      <td>2.157</td>
    </tr>
    <tr>
      <th>2</th>
      <td>AF</td>
      <td>DZA</td>
      <td>Algeria</td>
      <td>2.514</td>
    </tr>
    <tr>
      <th>3</th>
      <td>OC</td>
      <td>ASM</td>
      <td>American Samoa</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4</th>
      <td>EU</td>
      <td>AND</td>
      <td>Andorra</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>217</th>
      <td>AS</td>
      <td>UZB</td>
      <td>Uzbekistan</td>
      <td>2.580</td>
    </tr>
    <tr>
      <th>218</th>
      <td>SA</td>
      <td>VEN</td>
      <td>Venezuela, RB</td>
      <td>2.822</td>
    </tr>
    <tr>
      <th>219</th>
      <td>OC</td>
      <td>WSM</td>
      <td>Samoa</td>
      <td>4.503</td>
    </tr>
    <tr>
      <th>220</th>
      <td>AS</td>
      <td>YEM</td>
      <td>Yemen, Rep.</td>
      <td>6.313</td>
    </tr>
    <tr>
      <th>221</th>
      <td>AF</td>
      <td>ZMB</td>
      <td>Zambia</td>
      <td>6.036</td>
    </tr>
  </tbody>
</table>
<p>222 rows × 4 columns</p>
</div>




```python
OldToNew_fert={fert.columns[2]:'Country'}

OldToNew_fert

fert.rename(columns=OldToNew_fert)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>ContinentCode</th>
      <th>CountryCode</th>
      <th>Country</th>
      <th>FertilityRate</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>AS</td>
      <td>AFG</td>
      <td>Afghanistan</td>
      <td>7.485</td>
    </tr>
    <tr>
      <th>1</th>
      <td>EU</td>
      <td>ALB</td>
      <td>Albania</td>
      <td>2.157</td>
    </tr>
    <tr>
      <th>2</th>
      <td>AF</td>
      <td>DZA</td>
      <td>Algeria</td>
      <td>2.514</td>
    </tr>
    <tr>
      <th>3</th>
      <td>OC</td>
      <td>ASM</td>
      <td>American Samoa</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4</th>
      <td>EU</td>
      <td>AND</td>
      <td>Andorra</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>217</th>
      <td>AS</td>
      <td>UZB</td>
      <td>Uzbekistan</td>
      <td>2.580</td>
    </tr>
    <tr>
      <th>218</th>
      <td>SA</td>
      <td>VEN</td>
      <td>Venezuela, RB</td>
      <td>2.822</td>
    </tr>
    <tr>
      <th>219</th>
      <td>OC</td>
      <td>WSM</td>
      <td>Samoa</td>
      <td>4.503</td>
    </tr>
    <tr>
      <th>220</th>
      <td>AS</td>
      <td>YEM</td>
      <td>Yemen, Rep.</td>
      <td>6.313</td>
    </tr>
    <tr>
      <th>221</th>
      <td>AF</td>
      <td>ZMB</td>
      <td>Zambia</td>
      <td>6.036</td>
    </tr>
  </tbody>
</table>
<p>222 rows × 4 columns</p>
</div>




```python
fert.rename(columns=OldToNew_fert,inplace=True)
```


```python
fert.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>ContinentCode</th>
      <th>CountryCode</th>
      <th>Country</th>
      <th>FertilityRate</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>AS</td>
      <td>AFG</td>
      <td>Afghanistan</td>
      <td>7.485</td>
    </tr>
    <tr>
      <th>1</th>
      <td>EU</td>
      <td>ALB</td>
      <td>Albania</td>
      <td>2.157</td>
    </tr>
    <tr>
      <th>2</th>
      <td>AF</td>
      <td>DZA</td>
      <td>Algeria</td>
      <td>2.514</td>
    </tr>
    <tr>
      <th>3</th>
      <td>OC</td>
      <td>ASM</td>
      <td>American Samoa</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4</th>
      <td>EU</td>
      <td>AND</td>
      <td>Andorra</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
dirtyMerge = intermort.merge(fert,how='outer',indicator=True)
```


```python
dirtyMerge
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Country</th>
      <th>Usage</th>
      <th>Gender</th>
      <th>Value</th>
      <th>ContinentCode</th>
      <th>CountryCode</th>
      <th>FertilityRate</th>
      <th>_merge</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Albania</td>
      <td>0.114097</td>
      <td>Female</td>
      <td>103.0</td>
      <td>EU</td>
      <td>ALB</td>
      <td>2.157</td>
      <td>both</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Algeria</td>
      <td>0.491706</td>
      <td>Female</td>
      <td>138.0</td>
      <td>AF</td>
      <td>DZA</td>
      <td>2.514</td>
      <td>both</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Andorra</td>
      <td>10.538836</td>
      <td>Female</td>
      <td>50.0</td>
      <td>EU</td>
      <td>AND</td>
      <td>NaN</td>
      <td>both</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Angola</td>
      <td>0.105046</td>
      <td>Female</td>
      <td>390.0</td>
      <td>AF</td>
      <td>AGO</td>
      <td>6.639</td>
      <td>both</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Antigua and Barbuda</td>
      <td>6.482226</td>
      <td>Female</td>
      <td>148.0</td>
      <td>NA</td>
      <td>ATG</td>
      <td>2.200</td>
      <td>both</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>237</th>
      <td>Egypt, Arab Rep.</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>AF</td>
      <td>EGY</td>
      <td>3.340</td>
      <td>right_only</td>
    </tr>
    <tr>
      <th>238</th>
      <td>Isle of Man</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>EU</td>
      <td>IMN</td>
      <td>NaN</td>
      <td>right_only</td>
    </tr>
    <tr>
      <th>239</th>
      <td>Virgin Islands (U.S.)</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NA</td>
      <td>VIR</td>
      <td>2.060</td>
      <td>right_only</td>
    </tr>
    <tr>
      <th>240</th>
      <td>Venezuela, RB</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>SA</td>
      <td>VEN</td>
      <td>2.822</td>
      <td>right_only</td>
    </tr>
    <tr>
      <th>241</th>
      <td>Yemen, Rep.</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>AS</td>
      <td>YEM</td>
      <td>6.313</td>
      <td>right_only</td>
    </tr>
  </tbody>
</table>
<p>242 rows × 8 columns</p>
</div>




```python
#Look where hdi data frame found no match
dirtyMerge.loc[dirtyMerge['_merge']=='left_only',"Country"]
```




    12                                Bahamas
    32                             Cape Verde
    38                                  Congo
    39     Congo (Democratic Republic of the)
    47            Dem. People's Rep. of Korea
    51                         Dominican Rep.
    53                                  Egypt
    63                                 Gambia
    80                 Iran (Islamic Rep. of)
    92                             Kyrgyzstan
    93                             Lao P.D.R.
    134                                Russia
    136                 Saint Kitts and Nevis
    137                           Saint Lucia
    155                             Swaziland
    158                                 Syria
    159                    T.F.Y.R. Macedonia
    179                             Venezuela
    180                              Viet Nam
    181                                 Yemen
    Name: Country, dtype: object




```python
#Look where hdi data frame found no match
dirtyMerge.loc[dirtyMerge['_merge']=='right_only',"Country"]
```




    184                  Afghanistan
    185               American Samoa
    186                 Bahamas, The
    187                      Bermuda
    188       British Virgin Islands
    189                      Myanmar
    190                   Cabo Verde
    191               Cayman Islands
    192     Central African Republic
    193                  Congo, Rep.
    194             Congo, Dem. Rep.
    195           Dominican Republic
    196                Faroe Islands
    197             French Polynesia
    198                  Gambia, The
    199                    Gibraltar
    200                    Greenland
    201                         Guam
    202         Hong Kong SAR, China
    203           Iran, Islamic Rep.
    204                         Iraq
    205    Korea, Dem. People's Rep.
    206                  Korea, Rep.
    207              Kyrgyz Republic
    208                      Lao PDR
    209                Liechtenstein
    210             Macao SAR, China
    211                   Montenegro
    212                        Nauru
    213                      Curacao
    214                        Aruba
    215    Sint Maarten (Dutch part)
    216                New Caledonia
    217     Northern Mariana Islands
    218        Micronesia, Fed. Sts.
    219                        Palau
    220                     Pakistan
    221           West Bank and Gaza
    222                  Timor-Leste
    223                  Puerto Rico
    224           Russian Federation
    225           Russian Federation
    226          St. Kitts and Nevis
    227                    St. Lucia
    228     St. Martin (French part)
    229                       Serbia
    230              Slovak Republic
    231                      Vietnam
    232                  South Sudan
    233                     Eswatini
    234         Syrian Arab Republic
    235     Turks and Caicos Islands
    236              North Macedonia
    237             Egypt, Arab Rep.
    238                  Isle of Man
    239        Virgin Islands (U.S.)
    240                Venezuela, RB
    241                  Yemen, Rep.
    Name: Country, dtype: object




```python
replacements2 = {"Bahamas":"Bahamas, The","Congo":"Congo, Rep.", "Congo (Democratic Republic of the)":"Congo, Dem. Rep."," Dem. People's Rep. of Korea":"Korea, Dem. People's Rep.","Dominican Rep.":"Dominican Republic","Egypt":"Egypt, Arab Rep.","Gambia":"Gambia, The","Iran(Islamic Rep. of)":"Iran, Islamic Rep.","Kyrgyzstan":"Kyrgyz Republic","Russia": "Russian Federation", "Saint Kitts and Nevis":"St. Kitts and Nevis","Saint Lucia":"St. Lucia","Syria":"Syrian Arab Republic","T.F.Y.R. Macedonia":"North Macedonia","Venezuela":"Venezuela, RB","Viet Nam":"Vietnam","Yemen":"Yemen, Rep."}
```


```python
replacements2
```




    {'Bahamas': 'Bahamas, The',
     'Congo': 'Congo, Rep.',
     'Congo (Democratic Republic of the)': 'Congo, Dem. Rep.',
     " Dem. People's Rep. of Korea": "Korea, Dem. People's Rep.",
     'Dominican Rep.': 'Dominican Republic',
     'Egypt': 'Egypt, Arab Rep.',
     'Gambia': 'Gambia, The',
     'Iran(Islamic Rep. of)': 'Iran, Islamic Rep.',
     'Kyrgyzstan': 'Kyrgyz Republic',
     'Russia': 'Russian Federation',
     'Saint Kitts and Nevis': 'St. Kitts and Nevis',
     'Saint Lucia': 'St. Lucia',
     'Syria': 'Syrian Arab Republic',
     'T.F.Y.R. Macedonia': 'North Macedonia',
     'Venezuela': 'Venezuela, RB',
     'Viet Nam': 'Vietnam',
     'Yemen': 'Yemen, Rep.'}




```python
# replacing
fert.Country.replace(replacements2,inplace=True)
                     

```


```python
merged = intermort.merge(fert)
```


```python
merged
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Country</th>
      <th>Usage</th>
      <th>Gender</th>
      <th>Value</th>
      <th>ContinentCode</th>
      <th>CountryCode</th>
      <th>FertilityRate</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Albania</td>
      <td>0.114097</td>
      <td>Female</td>
      <td>103</td>
      <td>EU</td>
      <td>ALB</td>
      <td>2.157</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Algeria</td>
      <td>0.491706</td>
      <td>Female</td>
      <td>138</td>
      <td>AF</td>
      <td>DZA</td>
      <td>2.514</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Andorra</td>
      <td>10.538836</td>
      <td>Female</td>
      <td>50</td>
      <td>EU</td>
      <td>AND</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Angola</td>
      <td>0.105046</td>
      <td>Female</td>
      <td>390</td>
      <td>AF</td>
      <td>AGO</td>
      <td>6.639</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Antigua and Barbuda</td>
      <td>6.482226</td>
      <td>Female</td>
      <td>148</td>
      <td>NA</td>
      <td>ATG</td>
      <td>2.200</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>159</th>
      <td>Uruguay</td>
      <td>10.539058</td>
      <td>Female</td>
      <td>90</td>
      <td>SA</td>
      <td>URY</td>
      <td>2.237</td>
    </tr>
    <tr>
      <th>160</th>
      <td>Uzbekistan</td>
      <td>0.484347</td>
      <td>Female</td>
      <td>151</td>
      <td>AS</td>
      <td>UZB</td>
      <td>2.580</td>
    </tr>
    <tr>
      <th>161</th>
      <td>Vanuatu</td>
      <td>2.108337</td>
      <td>Female</td>
      <td>162</td>
      <td>OC</td>
      <td>VUT</td>
      <td>4.492</td>
    </tr>
    <tr>
      <th>162</th>
      <td>Zambia</td>
      <td>0.191072</td>
      <td>Female</td>
      <td>633</td>
      <td>AF</td>
      <td>ZMB</td>
      <td>6.036</td>
    </tr>
    <tr>
      <th>163</th>
      <td>Zimbabwe</td>
      <td>0.401434</td>
      <td>Female</td>
      <td>764</td>
      <td>AF</td>
      <td>ZWE</td>
      <td>3.748</td>
    </tr>
  </tbody>
</table>
<p>164 rows × 7 columns</p>
</div>




```python
merged.drop(columns='Gender', inplace=True)
```


```python
merged
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Country</th>
      <th>Usage</th>
      <th>Value</th>
      <th>ContinentCode</th>
      <th>CountryCode</th>
      <th>FertilityRate</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Albania</td>
      <td>0.114097</td>
      <td>103</td>
      <td>EU</td>
      <td>ALB</td>
      <td>2.157</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Algeria</td>
      <td>0.491706</td>
      <td>138</td>
      <td>AF</td>
      <td>DZA</td>
      <td>2.514</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Andorra</td>
      <td>10.538836</td>
      <td>50</td>
      <td>EU</td>
      <td>AND</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Angola</td>
      <td>0.105046</td>
      <td>390</td>
      <td>AF</td>
      <td>AGO</td>
      <td>6.639</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Antigua and Barbuda</td>
      <td>6.482226</td>
      <td>148</td>
      <td>NA</td>
      <td>ATG</td>
      <td>2.200</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>159</th>
      <td>Uruguay</td>
      <td>10.539058</td>
      <td>90</td>
      <td>SA</td>
      <td>URY</td>
      <td>2.237</td>
    </tr>
    <tr>
      <th>160</th>
      <td>Uzbekistan</td>
      <td>0.484347</td>
      <td>151</td>
      <td>AS</td>
      <td>UZB</td>
      <td>2.580</td>
    </tr>
    <tr>
      <th>161</th>
      <td>Vanuatu</td>
      <td>2.108337</td>
      <td>162</td>
      <td>OC</td>
      <td>VUT</td>
      <td>4.492</td>
    </tr>
    <tr>
      <th>162</th>
      <td>Zambia</td>
      <td>0.191072</td>
      <td>633</td>
      <td>AF</td>
      <td>ZMB</td>
      <td>6.036</td>
    </tr>
    <tr>
      <th>163</th>
      <td>Zimbabwe</td>
      <td>0.401434</td>
      <td>764</td>
      <td>AF</td>
      <td>ZWE</td>
      <td>3.748</td>
    </tr>
  </tbody>
</table>
<p>164 rows × 6 columns</p>
</div>




```python
merged.dtypes
```




    Country           object
    Usage            float64
    Value              int64
    ContinentCode     object
    CountryCode       object
    FertilityRate    float64
    dtype: object




```python
OldToNew3={merged.columns[1]:'%InternetUsage', merged.columns[2]:'MortalityRate'}

OldToNew3

merged.rename(columns=OldToNew3)

merged.rename(columns=OldToNew3,inplace=True)
```


```python
merged
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Country</th>
      <th>%InternetUsage</th>
      <th>MortalityRate</th>
      <th>ContinentCode</th>
      <th>CountryCode</th>
      <th>FertilityRate</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Albania</td>
      <td>0.114097</td>
      <td>103</td>
      <td>EU</td>
      <td>ALB</td>
      <td>2.157</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Algeria</td>
      <td>0.491706</td>
      <td>138</td>
      <td>AF</td>
      <td>DZA</td>
      <td>2.514</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Andorra</td>
      <td>10.538836</td>
      <td>50</td>
      <td>EU</td>
      <td>AND</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Angola</td>
      <td>0.105046</td>
      <td>390</td>
      <td>AF</td>
      <td>AGO</td>
      <td>6.639</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Antigua and Barbuda</td>
      <td>6.482226</td>
      <td>148</td>
      <td>NA</td>
      <td>ATG</td>
      <td>2.200</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>159</th>
      <td>Uruguay</td>
      <td>10.539058</td>
      <td>90</td>
      <td>SA</td>
      <td>URY</td>
      <td>2.237</td>
    </tr>
    <tr>
      <th>160</th>
      <td>Uzbekistan</td>
      <td>0.484347</td>
      <td>151</td>
      <td>AS</td>
      <td>UZB</td>
      <td>2.580</td>
    </tr>
    <tr>
      <th>161</th>
      <td>Vanuatu</td>
      <td>2.108337</td>
      <td>162</td>
      <td>OC</td>
      <td>VUT</td>
      <td>4.492</td>
    </tr>
    <tr>
      <th>162</th>
      <td>Zambia</td>
      <td>0.191072</td>
      <td>633</td>
      <td>AF</td>
      <td>ZMB</td>
      <td>6.036</td>
    </tr>
    <tr>
      <th>163</th>
      <td>Zimbabwe</td>
      <td>0.401434</td>
      <td>764</td>
      <td>AF</td>
      <td>ZWE</td>
      <td>3.748</td>
    </tr>
  </tbody>
</table>
<p>164 rows × 6 columns</p>
</div>




```python
#For use in R:
import rpy2
from rpy2.robjects import pandas2ri
pandas2ri.activate()

from rpy2.robjects.packages import importr

base = importr('base')
base.saveRDS(merged,file="TEAMdata.RDS")

```




    rpy2.rinterface.NULL


