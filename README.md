```julia
using Dates

Base.@kwdef struct Datseris
    job::String = "physicist"
    bdate::Int = 1991
    website::String = "https://datseris.github.io/"
    current_projects::Vector{String}
end

age(d) = Dates.year(now()) - d.bdate
Base.summary(d::Datseris) = "Some $(age(d)) year old $(d.job)"
workson(d::Datseris) = d.current_projects 
hobbies(::Datseris) = ("drums", "bouldering", "painting", "cooking", "programming")
favorite_project(::Datseris) = "DynamicalBilliards.jl"

# Begin my description
me = Datseris(current_projects = [
  "Stratocumulus-cumulus Transitions",
  "Global continuation",
  "Nonlinear response of dynamical systems",
  "DynamicalSystems.jl",
  "DrWatson.jl"
])

println(summary(me))
println("works on: $(join(me.current_projects, ", "))")
println("has hobbies: $(join(hobbies(me), ", "))")
```

![Datseris's github stats](https://github-readme-stats.vercel.app/api?username=Datseris&show_icons=true&hide=["issues"])

