# InLine-AsyncTask

1. The Basic
```
new AsyncTask<Void, Void, Void>() {
        protected void onPreExecute() {
                // Pre Code
        }
        protected Void doInBackground(Void... unused) {
                // Background Code
                return null;
        }
        protected void onPostExecute(Void unused) {
                // Post Code
        }
}.execute();
```

2. Return msg from doInBackground to onPostExecute
```
new AsyncTask<Void, Void, String>() {
        protected String doInBackground(Void... params) {
                return "message";
        }
        protected void onPostExecute(String msg) {
              
              Log.e("TAG",msg) 
        }
}.execute();
```
