# Retrieve Values from JSON

```
string json = "{"doc":"2121","serie":"0","num":"1"}";
JObject data = JObject.Parse(json);
-- or --
Object json = <<JSON Object received from POST>>
JObject data = JObject.Parse(json.ToString());

string transDoc = data["doc"].ToString();
string transSerie = data["serie"].ToString();
string transNum = data["num"].ToString();
return transDoc;
```