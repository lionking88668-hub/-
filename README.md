# -
python 控制结构作业
exchange_rate = 7.3795
while True:
    amount = input('请输入金额(以￥或$开头)：')
    try:
        y = float(amount[1:])
    except ValueError:
        print('输入错误，请重新输入')
        continue
    if y <= 0:
        print('数据有误')
        continue
    else:
        if amount.startswith('$'):
            a = y * exchange_rate
            print(f'{y} 美金换算人民币金额为{a:.2f}')
        elif amount.startswith('￥'):
            a = y / exchange_rate
            print(f'{y}人民币换算美金金额为{a:.2f}')
