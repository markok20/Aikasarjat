# Aikasarjat
Aikasarja-analyytiikkaa kolmesta eri näkökulmasta
Aikasarjaennustaminen - ei trendiä eikä kausivaihtelua
Aikasarjaennustaminen - trendi
Aikasarjaennustaminen - trendi ja kausivaihtelu

1 Datana lentomatkustajien lukumääriä. 
Lähde: https://www.kaggle.com/rakannimer/air-passengers
Aukeni säädylliseen dataframeen seuraavasti:
df=pd.read_csv('http://taanila.fi/AirPassengers.csv')
df.index=pd.to_datetime(df['Month'],format='%Y-%m')
df=df.drop('Month',axis=1)
df.head()

2 Ilman CO2-pitoisuuksia kuukausittain. Siististi käyttäytyvä aikasarja, jolle saa laskettua tarkkoja ennusteita.
Lähde: ftp://aftp.cmdl.noaa.gov/products/trends/co2/co2_mm_mlo.txt
Aukenee säädylliseen dataframeen seuraavasti:
df=pd.read_excel('http://taanila.fi/CO2.xlsx')
df.index = pd.to_datetime(df['Kuukausi'],format="%Y-%m")
df=df.drop('Kuukausi',axis=1)
df.head()

3 Oluen tuotantomääriä.
Lähde: https://www.kaggle.com/shenba/time-series-datasets
Aukenee säädylliseen dataframeen seuraavasti:
df=pd.read_csv('http://taanila.fi/beer.csv')
df.index=pd.to_datetime(df['Month'],format='%Y-%m')
df=df.drop('Month',axis=1)
df.head()

4 Sähkön tuotantoa.
Lähde: https://www.kaggle.com/shenba/time-series-datasets
Aukenee säädylliseen dataframeen seuraavasti:
df=pd.read_csv('http://taanila.fi/Electric_Production.csv')
df.index=pd.to_datetime(df['DATE'],format='%m/%d/%Y')
df=df.drop('DATE',axis=1)
df.head()
