# Verificar-que-el-activity-existe-Android

```
Activity activity = getActivity();
if(activity != null){

    // etc ...

}

EJEMPLO:

@Override
public void onError(VolleyError error) {

    Activity activity = getActivity(); 
    if(activity != null && isAdded())
        mProgressDialog.setVisibility(View.GONE);
        if (error instanceof NoConnectionError) {
           String errormsg = getResources().getString(R.string.no_internet_error_msg);
           Toast.makeText(activity, errormsg, Toast.LENGTH_LONG).show();
        }
    }
}

```

- También, usar isAdded()en el onError()método también:
