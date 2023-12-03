import pandas as pd

def print_top10_player(df):
    year_2015_2018 = df[df['year'].isin([2015, 2016, 2017, 2018])]
    sort_by_H = year_2015_2018.sort_values(by = 'H', ascending = False).batter_name.unique()[:10]
    print(f'top 10 players in hits {sort_by_H}')
    sort_by_avg = year_2015_2018.sort_values(by = 'avg', ascending = False).batter_name.unique()[:10]
    print(f'top 10 players in batting average {sort_by_avg}')
    sort_by_HR = year_2015_2018.sort_values(by = 'HR', ascending = False).batter_name.unique()[:10]
    print(f'top 10 players in homerun {sort_by_HR}')
    sort_by_OBP = year_2015_2018.sort_values(by = 'OBP', ascending = False).batter_name.unique()[:10]
    print(f'top 10 players in on-base percentage {sort_by_OBP}')

def print_hightest_war_by_position(df):
    year_2018 = df[df['year'] == 2018]
    highest_war_포수 = year_2018[year_2018['cp'] == '포수'].sort_values(by = 'war', ascending = False).batter_name.iloc[0]
    print(f'player with the highest war by position(포수): {highest_war_포수}')

    highest_war_1루수 = year_2018[year_2018['cp'] == '1루수'].sort_values(by = 'war', ascending = False).batter_name.iloc[0]
    print(f'player with the highest war by position(1루수): {highest_war_1루수}')

    highest_war_2루수 = year_2018[year_2018['cp'] == '2루수'].sort_values(by = 'war', ascending = False).batter_name.iloc[0]
    print(f'player with the highest war by position(2루수): {highest_war_2루수}')

    highest_war_3루수 = year_2018[year_2018['cp'] == '3루수'].sort_values(by = 'war', ascending = False).batter_name.iloc[0]
    print(f'player with the highest war by position(3루수): {highest_war_3루수}')

    highest_war_유격수 = year_2018[year_2018['cp'] == '유격수'].sort_values(by = 'war', ascending = False).batter_name.iloc[0]
    print(f'player with the highest war by position(유격수): {highest_war_유격수}')

    highest_war_좌익수 = year_2018[year_2018['cp'] == '좌익수'].sort_values(by = 'war', ascending = False).batter_name.iloc[0]
    print(f'player with the highest war by position(좌익수): {highest_war_좌익수}')

    highest_war_중견수 = year_2018[year_2018['cp'] == '중견수'].sort_values(by = 'war', ascending = False).batter_name.iloc[0]
    print(f'player with the highest war by position(중견수): {highest_war_중견수}')

    highest_war_우익수 = year_2018[year_2018['cp'] == '우익수'].sort_values(by = 'war', ascending = False).batter_name.iloc[0]
    print(f'player with the highest war by position(우익수): {highest_war_우익수}')

def highest_correlation(df):
    among = ['R', 'H', 'HR', 'RBI', 'SB', 'war', 'avg', 'OBP', 'SLG']
    corr = []
    for a in among:
        corr.append(df[a].corr(df['salary']))
    obj = pd.Series(corr, index = among)
    print(f'{obj.idxmax()} has the highest correlation with salary')

data_df = pd.read_csv('2019_kbo_for_kaggle_v2.csv')
print_top10_player(data_df)
print()
print_hightest_war_by_position(data_df)
print()
highest_correlation(data_df)
print()

