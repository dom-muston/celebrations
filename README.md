# Celebrations

ds <- data.frame(
    years1 = 2015:2025-2020,
    chocs = c(82,84,76,72,72,71,72,73,65,61,54)
    )


mod_null <- glm(chocs~1, family=poisson, data=ds)
coef(mod_null)

mod_year1 <- glm(chocs~years1, family=poisson, data=ds)
coef(mod_year1)

ds$years2 <- ds$years1^2
mod_year2 <- glm(chocs~years1+years2, family=poisson, data=ds)
coef(mod_year2)# celebrations
