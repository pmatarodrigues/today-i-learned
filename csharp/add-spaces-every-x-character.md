# Add space to String once between every X characters

```

String phoneNumber = "966666666";
int interval = 3;
String character = " ";

for (int i = interval; i <= phoneNumber.Length; i += interval)
{
  phoneNumber = phoneNumber.Insert(i, character);
  i++;
}

```

This was learned with the help of [DhavalR](https://stackoverflow.com/a/27977255)