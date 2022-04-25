# Hilt_MVVM_RoomDB_Retrofit
Refer the official documantation.

<li>Hilt is a dependency injection library for Android</li>
<li>Standard way of implementing DI in android</li>
<li>Built on top of Dagger 2</li>
<li> Hilt generates Dagger code for us</li>
<li>We just need to pass module for providing dependencies</li>

# @Inject (Class we will use as Dependency)
let say we have UserRepository we want to use as dependency in our application
<br>

class UserRepository @Inject constructor(){
//function....
}

# @HiltAndroidApp

Hilt required a application class which would be annoteted with @HiltAndroidApp


@HiltAndroidApp<br>
class UserApplication : Application(){
<br>
}
<br>
Behind the sceen it create all the required dagger classes for us

# @AndroidEntryPoint

In MainActivity
<br>
@AndroidEntryPoint<br>
class MainActivity : AppCompactActivity(){
<br>
    @Inject<br>
    lateint var userRepository: UserRepossitory<br>
    
    onCreate{<br>
    userRepository.saveUser()<br>
    }
}



# @Provides

# @InstallIn

# @Binds



