# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Maximum likelihood estimation (MLE) of SVC (spatially varying coefficient) model Use SVC_mle (varycoef) With (In) R Software
install.packages("varycoef")
library("varycoef")
# Estimation Maximum likelihood estimation (MLE) of SVC (spatially varying coefficient) model Use SVC_mle (varycoef) With (In) R Software
SVC_mle_ = read.csv("https://raw.githubusercontent.com/timbulwidodostp/SVC_mle/main/SVC_mle/SVC_mle.csv", sep = ";")
SVC_mle <- SVC_mle_[, c("dist", "lime", "elev")]
SVC_mle$l_cad <- log(SVC_mle_$cadmium)
SVC_mle$lime <- as.numeric(as.character(SVC_mle_$lime))
locs <- as.matrix(SVC_mle_[, c("x", "y")])
SVC_mle <- SVC_mle(l_cad ~ ., data = SVC_mle, locs = locs, control = SVC_mle_control(profileLik = TRUE, parscale = TRUE))
summary(SVC_mle)
# Maximum likelihood estimation (MLE) of SVC (spatially varying coefficient) model Use SVC_mle (varycoef) With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished