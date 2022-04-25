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

# Modules
It is a method a method by which we can create objects.


# @Provides

# @InstallIn

# @Binds
when ever we want to bind interface with implementation we use @Bind annotation

# Qualifier (@Named("_name_"))
it is a tag 

# @HiltViewModel
we have to annote or viewModel with @HiltViewModel and also with @Inject so that hilt can understand and create the requied objects from view model.




