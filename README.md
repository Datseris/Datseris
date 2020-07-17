```julia
Base.@kwdef struct Datseris
    job::String = "physicist"
    years::Int = 29
    website::String = "https://datseris.github.io/"
    current_projects::Vector{String}
end

Base.summary(d::Datseris) = "Some $(d.years) year old $(d.job)"
workson(d::Datseris) = d.current_projects 
hobbies(::Datseris) = ("drums", "painting", "cooking", "programming")
favorite_project(::Datseris) = "DynamicalBilliards.jl"

# Begin my description
me = Datseris(current_projects = [
  "Albedo Symmetry", 
  "Musician Synchronization",
  "Agents.jl",
  "DynamicalSystems.jl",
  "DrWatson.jl"
])

println(summary(me))
println("works on: $(join(me.current_projects, ", "))")
println("has hobbies: $(join(hobbies(me), ", "))")
```

![Datseris's github stats](https://github-readme-stats.vercel.app/api?username=Datseris&show_icons=true&hide=["issues"])

