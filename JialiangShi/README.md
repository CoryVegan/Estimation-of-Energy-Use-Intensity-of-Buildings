# berdo2017 outliers

berdo = pd.read_csv("berdo2017.csv",encoding='latin-1')

berdo = berdo[berdo["Site EUI (kBTU/sf)"]!="Not Available"]

to_drop = [37, 47, 81, 493, 501, 942, 1001, 1056, 1329, 1521, 1658, 1794]  # These are the EUI outliers

to_drop += [274, 877, 1181, 1631, 1259, 1420]  # These are the year built outliers

berdo = berdo.drop(to_drop)
