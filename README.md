# parcel-delivery

# discovery-server
Discovery Server üçün Spring Eureka istifadə etmişik.
Discovery Service microservice daxilində olan service'lərin məlumatlarını tutmaqdır. Mikroservice arxitekturasında hər bir servisin  birdən çox kopyası ola bilər. Bu servislərin bir biri ilə əlaqə qurması gərəkir. Bir servis bir servisin hansı ip və port da çalışdığını bilmir. 
Discovery Service bu problemin həlli üçün vacibdir. İşləyən hər servis Discovery Service də qeydiyyatda olur və beləliklə hansı servisin ayaqda olduğunu və onların ip və port məlumatlarını özundə saxlayar. Buna görə də təkcə Discovery Server in main class'inda @EnableEurekaServer annotation'dan istifadə olunur digərlərində @EnableEurekaClient istifadə edilir.

# api-gateway
APİ-GATEWAY client'dən gələn istəkləri müvafiq porta yönləndirir. Yəni məsələn bizim bir neçə servisimiz var və bunlar fərqli portlardadı client hər hansısa servisin işinə müraciət edir, bu zaman həmin client əslində Api-gateway'ə müraciət edir və Api-gateway müavafiq olan servisə yönləndirmə edir.

# service
İçərisində müvafiq servislərin işlərini daşıyır. Bir birindən əlaqəsiz həm ayrılıqda həm burlikdə işləyə bilən servislərdir. 
