## Hi 👋
```java
@GetMapping("/profile") 
public Result<Person> getProfile(@RequestParam("name") String name) { 
    if (RODYA.equals(name)) { 
        Person person = Person.builder() 
            .name(RODYA) 
            .age(25) 
            .gender("boy") 
            .job("Backend intern at Supcon") 
            .skill("Java, Spring...") 
            .blog("https://www.rodya.me") 
            .hobby("Read, pretend to be a literary youth.") 
            .idol("non")
            .motto("Make object-oriented great again")
            .build(); 
        
        return Result.success(person); 
    } 
    
    return Result.error("Man!!! Don't you have a profile yourself?"); 
}
```
