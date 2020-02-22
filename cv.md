Nika Shkuratava
============
* Email: nika_shkuratava@email.com
* Phone: +375 29 0000000

Summary
----------
* 10+ years of programming experience with consistently increasing responsibilities in software design and development of applications for mobile and embedded systems;
* 5 years of experience in Android development;
* Strong proficiency in problem solving, initiative taking, time management;
* Domain experience in telecommunication technologies, embedded systems;
* _Interested in IoT and neural networks;_
* Ability to learn new technologies quickly and independently.

## Skills
* Java
* C++
* Python
* RxJava
* Retrofit
* ORMLite
* Dagger 2

###Code samples
```
package com.example.nikashkuratova.smsreader.utils;

import android.app.Activity;
import android.content.Context;
import android.content.SharedPreferences;

import com.example.nikashkuratova.smsreader.pojo.SmsCategory;
import com.google.gson.Gson;
import com.google.gson.reflect.TypeToken;

import java.util.ArrayList;

import static com.example.nikashkuratova.smsreader.utils.ObjectCreatorHelper.createDefaultCategories;

public final class SharedPrefHelper {

    public static final String CATEGORIES_LIST_KEY ="CategoriesList";

    public static void saveToSharedPref(ArrayList<SmsCategory> list, Activity activity) {
        SharedPreferences sharedPref = activity.getSharedPreferences("nika",Context.MODE_PRIVATE);
        SharedPreferences.Editor editor = sharedPref.edit();
        String categoriesListtoJson = new Gson().toJson(list);
        editor.putString(CATEGORIES_LIST_KEY, categoriesListtoJson);
        editor.apply();
    }

    public static ArrayList<SmsCategory> readFromSharedPref(Activity activity) {
        ArrayList<SmsCategory> smsCategory = new ArrayList<SmsCategory>();
        SharedPreferences sharedPref = activity.getSharedPreferences("nika",Context.MODE_PRIVATE);
        Gson gson = new Gson();
        String json = sharedPref.getString(CATEGORIES_LIST_KEY, "");
        if (json.isEmpty()) {
            smsCategory = createDefaultCategories();
        } else {
            smsCategory = gson.fromJson(json, new TypeToken<ArrayList<SmsCategory>>() {
            }.getType());
        }
        return smsCategory;
    }
}
```
Experience
---------
All projects could be found on [Github](https://github.com/nshkuratova/)

Education
---------
Belarussian State University - Applied Mathematics _2005-2010_ 

English
-------
Advanced