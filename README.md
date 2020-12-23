# Firebase Authentication errors translations
Firebase's Admin Authentication API Errors Translated for convenience of error handing.
https://firebase.google.com/docs/auth/admin/errors

## Example
    import auth from '@react-native-firebase/auth';
    import { firebaseAuthErrorsAR } from '../../components/AuthComponents/firebaseAuthErrorsTranslate';
   
    ...
   
    auth().signInWithEmailAndPassword(email, password)
        .then(async (result: any) => {
            console.log('Logged in Successfully!');
        })
        .catch((error: any) => {
            if(firebaseAuthErrorsAR.hasOwnProperty(error.code)) {
                setAlertText(firebaseAuthErrorsAR[error.code]);
            } else {
                setAlertText('Error not found in json');
            }
        })
