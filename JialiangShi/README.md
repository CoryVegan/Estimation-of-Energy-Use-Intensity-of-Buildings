# Dectect and remove berdo outliers.
### Normally, EUI will not be over 800. Just apply the following code.
    to_drop = []
    for key,value in berdo.iterrows():
        if value[index of EUI column]>800:
            to_drop.append(key)
    berdo = berdo.drop(to_drop)
    berdo.sort_values(by='Site EUI (kBTU/sf)', ascending=False)
