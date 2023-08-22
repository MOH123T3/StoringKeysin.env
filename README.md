# StoringKeysin.env
Storing Keys in .env file and get


- Make .env file in your flutter project.
- Add API key in .env file.
-      Exp  APIKey=a500b817-4a93-4798-aa4d-ffd01c615862

-  Go to android app build.gradle and past this line 
-     apply from: project(':flutter_config').projectDir.getPath() + "/dotenv.gradle"

 - import 'package:flutter_config/flutter_config.dart';
 - and  add -
void main() async {
  WidgetsFlutterBinding.ensureInitialized(); // Required by FlutterConfig
  await FlutterConfig.loadEnvVariables();

  runApp(MyApp());
}


-  You Get Api key  - FlutterConfig.get('APIKey')
 

