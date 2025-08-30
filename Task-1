SELECT 
    c.login AS courier_login,
    COUNT(o.track) AS orders_in_delivery
FROM "Couriers" c
JOIN "Orders" o ON c.id = o."courierId"
WHERE o."inDelivery" = TRUE
  AND o.cancelled = FALSE
  AND o.finished = FALSE
GROUP BY c.login
ORDER BY orders_in_delivery DESC;
