# Session8Assignment1

What is Shared Preferences.?

Shared Preferences are used to save and retrieve key, value pair data.

SharedPreferences values will persist across user sessions.

Data in shared preferences will be persistent even though user closes the application.

We can get values from Shared preferences using getSharedPreferences() method.



What values can be saved in SharedPreferences.

We use SharedPreferences to store data: booleans, floats, ints, longs, and strings.

/******* Create SharedPreferences *******/
    SharedPreferences pref = getApplicationContext().getSharedPreferences("MyPref", MODE_PRIVATE); 
    Editor editor = pref.edit();
 
 
/**************** Storing data as KEY/VALUE pair *******************/
    editor.putBoolean("key_name1", true);           // Saving boolean - true/false
    editor.putInt("key_name2", "int value");        // Saving integer
    editor.putFloat("key_name3", "float value");    // Saving float
    editor.putLong("key_name4", "long value");      // Saving long
    editor.putString("key_name5", "string value");  // Saving string
    // Save the changes in SharedPreferences
    editor.commit(); // commit changes
 
 
/**************** Get SharedPreferences data *******************/
// If value for key not exist then return second param value - In this case null
 
    pref.getBoolean("key_name1", null);         // getting boolean
    pref.getInt("key_name2", null);             // getting Integer
    pref.getFloat("key_name3", null);           // getting Float
    pref.getLong("key_name4", null);            // getting Long 
