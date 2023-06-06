import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sb

# 데이터를 가져옵니다
url = "https://ko.wikipedia.org/wiki/%EB%8C%80%ED%95%9C%EB%AF%BC%EA%B5%AD%EC%9D%98_%EC%9D%B8%EA%B5%AC"
table = pd.read_html(url)
df = table[4]

# "연도 (년)" 열을 숫자 값으로 변환합니다
df['연도 (년)'] = pd.to_numeric(df['연도 (년)'], errors='coerce')

# 그래프를 그립니다
plt.figure(figsize=(12, 6))
plt.xticks(range(2000, 2023), rotation=60)
sb.lineplot(data=df, x="연도 (년)", y="출생자수(명)")
plt.xlim(2000, 2022)  # x축 범위 제한을 설정합니다
plt.xlabel("연도")
plt.ylabel("출생자 수")
plt.title("2000년부터 2022년까지 대한민국의 출생률")
plt.show()
