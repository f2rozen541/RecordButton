# Record Button
[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)]()


 This is a library which can you create a record button view in android


# Download
#### 1.Add this in your root `build.gradle at the end of repositories:
    allprojects {
        repositories {
            ...
            maven { url "https://jitpack.io" }
        }
    }
  
#### 2.Add this dependency in your app level `build.gradle:
    dependencies {
        ...
       compile 'com.github.emrekose26:RecordButton:1.0.0'
    }


# Usage
### 1. In your layout XML file:
    <com.emrekose.recordbutton.RecordButton
        android:id="@+id/recordBtn"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        app:buttonGap="20"
        app:buttonRadius="100"
        app:maxMilisecond="10000"
        app:progressColor="@color/colorPrimary"
        app:progressStroke="15"
        app:recordIcon="@drawable/ic_keyboard_voice_white_36dp" />
  
### 2. In your class file:

    RecordButton recordButton = (RecordButton) findViewById(R.id.recordBtn);

        recordButton.setRecordListener(new OnRecordListener() {
            @Override
            public void onRecord() {
                Log.e(TAG, "onRecord: ");
            }

            @Override
            public void onRecordFinish() {
                Log.e(TAG, "onRecordFinish: ");
            }
        });
  

# License