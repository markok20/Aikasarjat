# Aikasarjat
Aikasarjat
Aikasarjaennustaminen - ei trendiä eikä kausivaihtelua
Aikasarjaennustaminen - trendi
Aikasarjaennustaminen - trendi ja kausivaihtelu

Datana lentomatkustajien lukumääriä. 
Lähde: https://www.kaggle.com/rakannimer/air-passengers

Aukeni säädylliseen dataframeen seuraavasti:

df=pd.read_csv('http://taanila.fi/AirPassengers.csv')
df.index=pd.to_datetime(df['Month'],format='%Y-%m')
df=df.drop('Month',axis=1)
df.head()
