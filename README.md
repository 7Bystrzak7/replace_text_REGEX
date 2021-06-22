# replace_text_REGEX

# zmiana ciagu tekstowego na liczbe(formatu float)

numberStr_delRegex_char = re.compile(r'[ zł]')
comma_dot_conversionRegex = re.compile(r'[,]')

wartosc_text = ['7 777,77 zł', '7,70 zł', '70,77 zł', ' 77 777,77 zł']



for i in wartosc_text:
    number_str = numberStr_delRegex_char.sub('', i)
    number = comma_dot_conversionRegex.sub('.', number_str)
    number_float = float(number)
    print(number_float)
